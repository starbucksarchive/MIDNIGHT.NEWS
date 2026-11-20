
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>MIDNIGHT NEWS. — Every hour has a story.</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --background: #080b09;
  --surface: #101612;
  --surface-light: #151d18;
  --green: #78d99a;
  --cream: #eeeade;
  --muted: #939b93;
  --line: rgba(120,217,154,0.25);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--background);
  color: var(--cream);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
}

button, input {
  font: inherit;
}

/* TOP BAR */

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 13px 6%;
  border-bottom: 1px solid var(--line);
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.clock-area {
  text-align: right;
}

/* MASTHEAD */

.masthead {
  text-align: center;
  padding: 38px 15px 27px;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-size: clamp(38px, 7vw, 76px);
  font-weight: 500;
  letter-spacing: 5px;
  line-height: 1.1;
}

.logo span {
  color: var(--green);
}

.tagline {
  margin-top: 12px;
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 5px;
  text-transform: uppercase;
}

/* NAVIGATION */

nav {
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 34px;
  padding: 16px 12px;
}

nav a {
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted);
  transition: 0.25s;
}

nav a:hover {
  color: var(--green);
}

/* BREAKING STRIP */

.breaking {
  background: var(--green);
  color: #07100a;
  padding: 11px 6%;
  display: flex;
  align-items: center;
  gap: 15px;
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.breaking-label {
  font-weight: 700;
  border-right: 1px solid rgba(0,0,0,0.3);
  padding-right: 15px;
}

/* GENERAL */

.container {
  width: 88%;
  max-width: 1250px;
  margin: auto;
}

.section-heading {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 28px;
  font-size: 11px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--green);
}

.section-heading::after {
  content: "";
  height: 1px;
  background: var(--line);
  flex: 1;
}

/* COVER */

.cover {
  padding: 65px 0 75px;
}

.cover-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 45px;
  align-items: center;
}

.cover-image {
  width: 100%;
  height: 470px;
  object-fit: cover;
  background: var(--surface);
}

.cover-copy .eyebrow {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.cover-copy h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(38px, 5vw, 66px);
  line-height: 1.12;
  font-weight: 400;
  margin-bottom: 22px;
}

.cover-copy p {
  color: var(--muted);
  font-size: 14px;
  max-width: 450px;
}

.cover-note {
  display: inline-block;
  margin-top: 30px;
  color: var(--green);
  border-bottom: 1px solid var(--green);
  padding-bottom: 5px;
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
}

/* EMPTY NEWS SECTION */

.latest {
  padding: 65px 0;
  border-top: 1px solid var(--line);
}

.empty-news {
  border: 1px solid var(--line);
  background: var(--surface);
  padding: 65px 20px;
  text-align: center;
}

.empty-news h2 {
  font-family: 'Playfair Display', serif;
  font-size: 32px;
  font-weight: 400;
  margin-bottom: 10px;
}

.empty-news p {
  color: var(--muted);
  font-size: 13px;
}

/* SEARCH */

.search-section {
  padding: 45px 0;
  border-top: 1px solid var(--line);
}

.search-box {
  display: flex;
  gap: 12px;
  max-width: 600px;
}

.search-box input {
  width: 100%;
  padding: 14px 16px;
  color: var(--cream);
  background: var(--surface);
  border: 1px solid var(--line);
  outline: none;
}

.search-box input:focus {
  border-color: var(--green);
}

.search-box button,
.newsletter button {
  padding: 13px 22px;
  border: none;
  background: var(--green);
  color: #07100a;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 2px;
  cursor: pointer;
}

/* BOOKMARKS */

.bookmarks {
  padding: 45px 0;
  border-top: 1px solid var(--line);
}

.bookmark-list {
  color: var(--muted);
  font-size: 13px;
}

/* TRAVEL FEATURE */

.travel {
  padding: 75px 0;
  border-top: 1px solid var(--line);
}

.travel-label {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 15px;
}

.travel-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(34px, 5vw, 58px);
  line-height: 1.15;
  font-weight: 400;
  margin-bottom: 35px;
  max-width: 850px;
}

.travel-hero {
  width: 100%;
  height: min(720px, 75vw);
  min-height: 340px;
  object-fit: cover;
  object-position: center 35%;
  display: block;
  background: var(--surface);
}

.travel-caption {
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-top: 12px;
}

.travel-intro {
  max-width: 780px;
  margin: 35px auto 65px;
  font-family: 'Playfair Display', serif;
  font-size: 20px;
  line-height: 1.8;
  color: #d9d8ce;
  text-align: center;
}

/* VIDEOS */

.video-heading {
  font-family: 'Playfair Display', serif;
  font-size: 31px;
  font-weight: 400;
  margin-bottom: 28px;
}

.video-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 25px;
}

.video-card {
  background: var(--surface);
  border: 1px solid var(--line);
  padding: 12px;
}

.video-thumbnail {
  position: relative;
  display: block;
  overflow: hidden;
  aspect-ratio: 16 / 9;
  background: #151d18;
}

.video-thumbnail img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s;
}

.video-thumbnail:hover img {
  transform: scale(1.04);
}

.play-button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 55px;
  height: 55px;
  border-radius: 50%;
  background: rgba(8,11,9,0.8);
  border: 1px solid var(--green);
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--green);
  font-size: 18px;
}

.video-title {
  font-family: 'Playfair Display', serif;
  font-size: 19px;
  line-height: 1.4;
  font-weight: 400;
  margin: 17px 5px 7px;
}

.video-subtitle {
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin: 0 5px 8px;
}

/* SOCIAL LINKS */

.follow {
  border-top: 1px solid var(--line);
  margin-top: 65px;
  padding-top: 35px;
}

.follow h3 {
  font-size: 10px;
  color: var(--green);
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.social-links {
  display: flex;
  flex-wrap: wrap;
  gap: 25px;
}

.social-links a {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  color: var(--muted);
  font-size: 12px;
  transition: 0.25s;
}

.social-links a:hover {
  color: var(--green);
}

.social-links svg {
  width: 19px;
  height: 19px;
  fill: currentColor;
}

/* NEWSLETTER */

.newsletter {
  margin-top: 65px;
  padding: 55px 20px;
  background: var(--surface);
  border: 1px solid var(--line);
  text-align: center;
}

.newsletter h2 {
  font-family: 'Playfair Display', serif;
  font-size: 35px;
  font-weight: 400;
  margin-bottom: 10px;
}

.newsletter p {
  color: var(--muted);
  font-size: 13px;
  margin-bottom: 25px;
}

.newsletter form {
  display: flex;
  max-width: 460px;
  margin: auto;
  gap: 8px;
}

.newsletter input {
  flex: 1;
  min-width: 0;
  padding: 13px;
  background: var(--background);
  border: 1px solid var(--line);
  color: var(--cream);
  outline: none;
}

/* FOOTER */

footer {
  border-top: 1px solid var(--line);
  margin-top: 70px;
  padding: 30px 6%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 15px;
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
}

footer span {
  color: var(--green);
}

/* RESPONSIVE */

@media (max-width: 750px) {
  .topbar {
    font-size: 8px;
    letter-spacing: 1px;
  }

  nav {
    gap: 17px;
  }

  nav a {
    font-size: 9px;
  }

  .cover-grid {
    grid-template-columns: 1fr;
    gap: 25px;
  }

  .cover-image {
    height: 340px;
  }

  .cover {
    padding: 40px 0 55px;
  }

  .travel-hero {
    min-height: 300px;
  }

  .video-grid {
    grid-template-columns: 1fr;
  }

  .travel-intro {
    font-size: 17px;
    text-align: left;
  }

  .newsletter form {
    flex-direction: column;
  }

  .newsletter button {
    width: 100%;
  }

  footer {
    flex-direction: column;
  }
}
</style>
</head>

<body>

<!-- TOP BAR -->
<header class="topbar">
  <div>INDEPENDENT EDITORIAL JOURNAL</div>

  <div class="clock-area">
    <div id="clock">00:00:00 JST</div>
    <div id="date">TOKYO, JAPAN</div>
  </div>
</header>

<!-- MASTHEAD -->
<div class="masthead" id="home">
  <div class="logo">MIDNIGHT <span>NEWS.</span></div>
  <p class="tagline">Every hour has a story.</p>
</div>

<!-- NAVIGATION -->
<nav>
  <a href="#home">Home</a>
  <a href="#cover">Cover</a>
  <a href="#latest">Latest</a>
  <a href="#search">Search</a>
  <a href="#bookmarks">Bookmarks</a>
  <a href="#travel">Travel</a>
  <a href="#newsletter">Newsletter</a>
</nav>

<!-- BREAKING NEWS STRIP -->
<div class="breaking">
  <span class="breaking-label">BREAKING</span>
  <span>THE WORLD, ONE STORY AT A TIME.</span>
</div>

<!-- COVER -->
<main>

<section class="cover container" id="cover">
  <div class="cover-grid">

    <div>
      <img
        class="cover-image"
        src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=1400&q=85"
        alt="Editorial workspace"
      >
    </div>

    <div class="cover-copy">
      <div class="eyebrow">THE MIDNIGHT EDITION</div>

      <h1>A different perspective on the world.</h1>

      <p>
        A space for stories, ideas, discoveries and everything
        worth taking a closer look at.
      </p>

      <a class="cover-note" href="#latest">EXPLORE THE EDITION</a>
    </div>

  </div>
</section>

<!-- LATEST -->
<section class="latest container" id="latest">
  <div class="section-heading">THE LATEST</div>

  <div class="empty-news">
    <h2>Every hour has a story.</h2>
    <p>New stories will appear here soon.</p>
  </div>
</section>

<!-- SEARCH -->
<section class="search-section container" id="search">
  <div class="section-heading">SEARCH THE EDITION</div>

  <div class="search-box">
    <input
      type="search"
      id="searchInput"
      placeholder="Search Midnight News..."
      aria-label="Search Midnight News"
    >
    <button type="button" onclick="searchSite()">SEARCH</button>
  </div>

  <p id="searchMessage" style="color:var(--muted);font-size:12px;margin-top:14px;"></p>
</section>

<!-- BOOKMARKS -->
<section class="bookmarks container" id="bookmarks">
  <div class="section-heading">YOUR BOOKMARKS</div>
  <div class="bookmark-list" id="bookmarkList">
    Your saved stories will appear here.
  </div>
</section>

<!-- AMANDA KING TRAVEL FEATURE -->
<section class="travel container" id="travel">

  <div class="travel-label">
    TRAVEL & LIFESTYLE — CREATOR SPOTLIGHT
  </div>

  <h1 class="travel-title">
    MY FAVOURITE TRAVEL INFLUENCER — AMANDA KING
  </h1>

  <!-- STATIC IMAGE: DOES NOT LINK TO INSTAGRAM -->
 <img
  class="travel-hero"
  src="https://images.squarespace-cdn.com/content/v1/67eb60db253c5c45656397d2/a6fde003-084c-44bf-bf31-79ff9d02c3a4/DSC01393.JPG"
  alt="Amanda King"
>

  <div class="travel-caption">
    CREATOR SPOTLIGHT · AMANDA KING
  </div>

  <p class="travel-intro">
    Some creators inspire you to travel, explore and see the world differently.
    For me, Amanda King is one of those creators. Her travel videos, adventures
    and experiences make exploring the world even more exciting. That's why
    she is one of my favourite travel influencers.
  </p>

  <!-- YOUTUBE VIDEOS -->
  <h2 class="video-heading">A LITTLE MORE TO EXPLORE</h2>

  <div class="video-grid">

    <!-- VIDEO ONE -->
    <article class="video-card">

      <a
        class="video-thumbnail"
        href="https://www.youtube.com/watch?v=kCeeTUSm4eo"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="Watch Amanda King's first selected video on YouTube"
      >
        <img
          src="https://img.youtube.com/vi/kCeeTUSm4eo/hqdefault.jpg"
          alt="First Amanda King YouTube video thumbnail"
        >

        <span class="play-button">▶</span>
      </a>

      <p class="video-subtitle">SELECTED VIDEO · 01</p>

      <h3 class="video-title">
        Behind The Scenes as EMIRATES CABIN CREW - Things you DONT see as a Passenger - Shanghai Vlog
      </h3>

    </article>

    <!-- VIDEO TWO -->
    <article class="video-card">

      <a
        class="video-thumbnail"
        href="https://www.youtube.com/watch?v=_-b3kdiSETI"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="Watch Amanda King's second selected video on YouTube"
      >
        <img
          src="https://img.youtube.com/vi/_-b3kdiSETI/hqdefault.jpg"
          alt="Second Amanda King YouTube video thumbnail"
        >

        <span class="play-button">▶</span>
      </a>

      <p class="video-subtitle">SELECTED VIDEO · 02</p>

      <h3 class="video-title" id="secondVideoTitle">
        Selected video
      </h3>

    </article>

  </div>

  <!-- SOCIAL LINKS AT THE VERY END -->
  <div class="follow">

    <h3>FOLLOW AMANDA KING</h3>

    <div class="social-links">

      <a
        href="https://www.instagram.com/its.amandaking/"
        target="_blank"
        rel="noopener noreferrer"
      >
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <rect x="3" y="3" width="18" height="18" rx="5"
            fill="none" stroke="currentColor" stroke-width="1.8"/>
          <circle cx="12" cy="12" r="4"
            fill="none" stroke="currentColor" stroke-width="1.8"/>
          <circle cx="17.5" cy="6.5" r="1.1"/>
        </svg>
        Instagram · @its.amandaking
      </a>

      <a
        href="https://www.youtube.com/@its.amandaking"
        target="_blank"
        rel="noopener noreferrer"
      >
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M23 7.1a3 3 0 0 0-2.1-2.1C19 4.5 12 4.5 12 4.5s-7 0-8.9.5A3 3 0 0 0 1 7.1 31 31 0 0 0 .5 12a31 31 0 0 0 .5 4.9 3 3 0 0 0 2.1 2.1c1.9.5 8.9.5 8.9.5s7 0 8.9-.5a3 3 0 0 0 2.1-2.1 31 31 0 0 0 .5-4.9 31 31 0 0 0-.5-4.9ZM9.7 15.5v-7l6 3.5-6 3.5Z"/>
        </svg>
        YouTube · @its.amandaking
      </a>

    </div>
  </div>

</section>

<!-- NEWSLETTER -->
<section class="newsletter container" id="newsletter">

  <h2>The Midnight Letter.</h2>

  <p>A little something worth reading, delivered to your inbox.</p>

  <form id="newsletterForm">
    <input
      type="email"
      id="emailInput"
      placeholder="Your email address"
      required
    >

    <button type="submit">SUBSCRIBE</button>
  </form>

  <p id="newsletterMessage" style="margin-top:15px;"></p>

</section>

</main>

<!-- FOOTER -->
<footer>
  <div>© 2026 MIDNIGHT NEWS.</div>
  <div>EVERY HOUR HAS A <span>STORY.</span></div>
</footer>

<script>

/* JAPAN STANDARD TIME CLOCK */

function updateClock() {
  const now = new Date();

  document.getElementById("clock").textContent =
    new Intl.DateTimeFormat("en-GB", {
      timeZone: "Asia/Tokyo",
      hour: "2-digit",
      minute: "2-digit",
      second: "2-digit",
      hour12: false
    }).format(now) + " JST";

  document.getElementById("date").textContent =
    new Intl.DateTimeFormat("en-GB", {
      timeZone: "Asia/Tokyo",
      weekday: "long",
      day: "numeric",
      month: "long",
      year: "numeric"
    }).format(now).toUpperCase();
}

updateClock();
setInterval(updateClock, 1000);


/* SEARCH */

function searchSite() {
  const query = document
    .getElementById("searchInput")
    .value.trim();

  const message = document.getElementById("searchMessage");

  if (!query) {
    message.textContent = "Enter something to search.";
    return;
  }

  const travelMatch =
    "travel lifestyle creator spotlight amanda king"
    .includes(query.toLowerCase()) ||
    query.toLowerCase().split(" ").some(word =>
      ["travel", "amanda", "king", "creator", "lifestyle"].includes(word)
    );

  if (travelMatch) {
    message.textContent = "A matching feature was found.";
    document.getElementById("travel").scrollIntoView({
      behavior: "smooth"
    });
  } else {
    message.textContent = "No matching stories yet.";
  }
}

document.getElementById("searchInput").addEventListener("keydown", function(event) {
  if (event.key === "Enter") {
    searchSite();
  }
});


/* BOOKMARK STORAGE */

function displayBookmarks() {
  const saved = JSON.parse(localStorage.getItem("midnightBookmarks") || "[]");

  const list = document.getElementById("bookmarkList");

  if (saved.length === 0) {
    list.textContent = "Your saved stories will appear here.";
    return;
  }

  list.innerHTML = saved.map(item =>
    `<p>${escapeHTML(item)}</p>`
  ).join("");
}

function escapeHTML(value) {
  return String(value).replace(/[&<>"']/g, function(char) {
    return {
      "&": "&amp;",
      "<": "&lt;",
      ">": "&gt;",
      '"': "&quot;",
      "'": "&#39;"
    }[char];
  });
}

displayBookmarks();


/* NEWSLETTER DEMO */

document.getElementById("newsletterForm").addEventListener("submit", function(event) {
  event.preventDefault();

  document.getElementById("newsletterMessage").textContent =
    "Thank you for your interest in The Midnight Letter.";

  this.reset();
});


/* SECOND VIDEO TITLE */

fetch("https://www.youtube.com/oembed?url=" +
  encodeURIComponent("https://www.youtube.com/watch?v=_-b3kdiSETI") +
  "&format=json")
  .then(response => {
    if (!response.ok) throw new Error("Title unavailable");
    return response.json();
  })
  .then(data => {
    document.getElementById("secondVideoTitle").textContent = data.title;
  })
  .catch(() => {
    document.getElementById("secondVideoTitle").textContent = "Selected video";
  });

</script>

</body>
</html>
