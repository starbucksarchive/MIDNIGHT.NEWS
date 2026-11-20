
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>MIDNIGHT NEWS.</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --black: #080b09;
  --dark: #101712;
  --card: #131b15;
  --green: #78d99a;
  --deep-green: #163923;
  --cream: #f4f0e6;
  --muted: #929d94;
  --border: #29372d;
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
  background: var(--black);
  color: var(--cream);
  font-family: 'DM Sans', sans-serif;
}

/* HEADER */

header {
  text-align: center;
  padding: 38px 20px 25px;
  border-bottom: 1px solid var(--border);
}

.top-label {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 4px;
  margin-bottom: 17px;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-size: clamp(38px, 8vw, 76px);
  letter-spacing: 2px;
  font-weight: 600;
}

.logo span {
  color: var(--green);
}

.tagline {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  color: var(--muted);
  font-size: 15px;
  margin-top: 8px;
}

.header-date {
  margin-top: 19px;
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 2px;
}

/* NAVIGATION */

nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 30px;
  padding: 17px 15px;
  border-bottom: 1px solid var(--border);
}

nav a {
  color: var(--cream);
  text-decoration: none;
  font-size: 10px;
  letter-spacing: 2px;
  transition: .3s;
}

nav a:hover {
  color: var(--green);
}

/* BREAKING STRIP */

.breaking {
  display: flex;
  align-items: center;
  gap: 15px;
  padding: 13px 5%;
  background: var(--deep-green);
}

.breaking-label {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 2px;
  font-weight: 700;
  white-space: nowrap;
}

.breaking-text {
  color: var(--cream);
  font-size: 11px;
}

/* CLOCK */

.clock-section {
  text-align: center;
  padding: 40px 20px;
  border-bottom: 1px solid var(--border);
}

.clock-label {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 3px;
  margin-bottom: 12px;
}

.clock {
  font-family: 'Playfair Display', serif;
  font-size: clamp(35px, 7vw, 58px);
  letter-spacing: 3px;
}

.clock-note {
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  margin-top: 8px;
}

/* GENERAL SECTIONS */

section {
  padding: 55px 7%;
}

.section-heading {
  display: flex;
  align-items: center;
  gap: 18px;
  margin-bottom: 28px;
}

.section-heading h2 {
  font-family: 'Playfair Display', serif;
  font-size: 25px;
  font-weight: 500;
}

.section-heading span {
  height: 1px;
  background: var(--border);
  flex: 1;
}

/* MAIN COVER */

.cover {
  min-height: 390px;
  background: var(--dark);
  border: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 30px;
}

.cover-small {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 4px;
  margin-bottom: 20px;
}

.cover h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(35px, 6vw, 65px);
  font-weight: 400;
}

.cover p {
  color: var(--muted);
  font-size: 11px;
  letter-spacing: 3px;
  margin-top: 20px;
}

.cover-line {
  height: 1px;
  width: 75px;
  background: var(--green);
  margin-top: 25px;
}

/* LATEST STORIES */

.story-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.story-card {
  background: var(--card);
  border: 1px solid var(--border);
  min-height: 210px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  transition: .3s;
}

.story-card:hover {
  border-color: var(--green);
  transform: translateY(-4px);
}

.story-number {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 2px;
}

.story-card h3 {
  font-family: 'Playfair Display', serif;
  font-size: 23px;
  font-weight: 400;
  margin-top: 12px;
}

.story-card p {
  color: var(--muted);
  font-size: 11px;
  margin-top: 8px;
}

/* SEARCH */

.search-box {
  display: flex;
  gap: 10px;
  max-width: 600px;
  margin: auto;
}

.search-box input {
  flex: 1;
  min-width: 0;
  background: var(--dark);
  border: 1px solid var(--border);
  padding: 15px;
  color: var(--cream);
  outline: none;
  font-family: inherit;
}

.search-box input:focus {
  border-color: var(--green);
}

.search-box button {
  background: var(--green);
  color: var(--black);
  border: none;
  padding: 0 23px;
  font-weight: 700;
  cursor: pointer;
}

.search-message {
  text-align: center;
  color: var(--muted);
  font-size: 12px;
  margin-top: 15px;
}

/* BOOKMARKS */

.bookmark-area {
  border: 1px solid var(--border);
  background: var(--dark);
  padding: 30px;
  color: var(--muted);
  font-size: 12px;
  text-align: center;
}

/* NEWSLETTER */

.newsletter {
  background: var(--dark);
  border: 1px solid var(--border);
  padding: 40px 25px;
  text-align: center;
}

.newsletter h2 {
  font-family: 'Playfair Display', serif;
  font-size: 30px;
  font-weight: 400;
}

.newsletter p {
  color: var(--muted);
  font-size: 12px;
  margin: 12px 0 25px;
}

.newsletter form {
  display: flex;
  max-width: 450px;
  margin: auto;
  gap: 8px;
}

.newsletter input {
  flex: 1;
  min-width: 0;
  padding: 14px;
  background: var(--black);
  border: 1px solid var(--border);
  color: var(--cream);
}

.newsletter button {
  background: var(--green);
  color: var(--black);
  border: none;
  padding: 0 18px;
  font-weight: 700;
  cursor: pointer;
}

#newsletter-message {
  margin-top: 15px;
  color: var(--green);
  font-size: 12px;
}

/* AMANDA KING EDITORIAL */

.amanda-feature {
  --travel-cream: #eee9df;
  --travel-muted: #aaa99f;
  --travel-accent: #b6c5a3;
  --travel-line: rgba(238,233,223,.2);

  background: #111610;
  color: var(--travel-cream);
  padding: 75px 7%;
  margin-top: 35px;
}

.amanda-kicker {
  font-size: 10px;
  letter-spacing: 3px;
  color: var(--travel-accent);
  text-transform: uppercase;
  margin-bottom: 22px;
}

.amanda-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(38px, 6vw, 72px);
  line-height: 1.08;
  font-weight: 400;
  max-width: 900px;
}

.amanda-title em {
  color: var(--travel-accent);
  font-weight: 400;
}

.amanda-subtitle {
  color: var(--travel-muted);
  font-size: 10px;
  letter-spacing: 2px;
  margin-top: 22px;
}

.amanda-hero {
  margin-top: 42px;
  background: #20291f;
  overflow: hidden;
}

.amanda-hero img {
  display: block;
  width: 100%;
  height: clamp(280px, 52vw, 580px);
  object-fit: cover;
  object-position: center 35%;
  filter: brightness(.88);
}

.amanda-photo-caption {
  padding: 12px 0;
  color: var(--travel-muted);
  font-size: 10px;
  letter-spacing: 1px;
}

.amanda-intro {
  max-width: 760px;
  margin: 65px auto 75px;
  text-align: center;
}

.amanda-intro-label {
  color: var(--travel-accent);
  font-size: 10px;
  letter-spacing: 3px;
  margin-bottom: 24px;
}

.amanda-intro p {
  font-family: 'Playfair Display', serif;
  font-size: clamp(19px, 2.5vw, 27px);
  line-height: 1.8;
  font-weight: 400;
}

.amanda-divider {
  height: 1px;
  background: var(--travel-line);
  margin: 55px 0;
}

.amanda-video-heading {
  font-family: 'Playfair Display', serif;
  font-size: clamp(27px, 4vw, 39px);
  font-weight: 400;
  margin-bottom: 12px;
}

.amanda-video-note {
  color: var(--travel-muted);
  font-size: 11px;
  letter-spacing: 1px;
  margin-bottom: 32px;
}

.amanda-video-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 28px;
}

.amanda-video-card {
  display: block;
  color: inherit;
  text-decoration: none;
}

.amanda-thumbnail {
  position: relative;
  overflow: hidden;
  background: #252c25;
  aspect-ratio: 16 / 9;
}

.amanda-thumbnail img {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  transition: transform .5s ease;
}

.amanda-video-card:hover .amanda-thumbnail img {
  transform: scale(1.04);
}

.amanda-play {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 62px;
  height: 62px;
  border: 1px solid rgba(255,255,255,.8);
  border-radius: 50%;
  display: grid;
  place-items: center;
  background: rgba(12,17,12,.55);
  transition: .3s;
}

.amanda-play svg {
  width: 20px;
  fill: white;
  margin-left: 4px;
}

.amanda-video-card:hover .amanda-play {
  background: var(--travel-accent);
  border-color: var(--travel-accent);
}

.amanda-video-card:hover .amanda-play svg {
  fill: #111610;
}

.amanda-video-meta {
  display: flex;
  gap: 12px;
  align-items: center;
  margin-top: 17px;
  color: var(--travel-accent);
  font-size: 9px;
  letter-spacing: 2px;
}

.amanda-video-title {
  font-family: 'Playfair Display', serif;
  font-size: 20px;
  font-weight: 400;
  line-height: 1.4;
  margin-top: 9px;
}

.amanda-video-open {
  color: var(--travel-muted);
  font-size: 10px;
  margin-top: 9px;
  letter-spacing: 1px;
}

.amanda-follow {
  text-align: center;
  padding-top: 10px;
}

.amanda-follow h3 {
  font-family: 'Playfair Display', serif;
  font-size: 32px;
  font-weight: 400;
  margin-bottom: 28px;
}

.amanda-socials {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 14px;
}

.amanda-social-link {
  display: flex;
  align-items: center;
  gap: 12px;
  border: 1px solid var(--travel-line);
  padding: 15px 22px;
  color: var(--travel-cream);
  text-decoration: none;
  font-size: 11px;
  letter-spacing: 1px;
  transition: .3s;
}

.amanda-social-link:hover {
  border-color: var(--travel-accent);
  color: var(--travel-accent);
}

.amanda-social-link svg {
  width: 19px;
  height: 19px;
  fill: none;
  stroke: currentColor;
  stroke-width: 1.6;
}

/* FOOTER */

footer {
  border-top: 1px solid var(--border);
  padding: 30px 20px;
  text-align: center;
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
}

footer span {
  color: var(--green);
}

/* RESPONSIVE */

@media (max-width: 700px) {
  nav {
    gap: 17px;
  }

  section {
    padding: 40px 6%;
  }

  .story-grid {
    grid-template-columns: 1fr;
  }

  .cover {
    min-height: 320px;
  }

  .amanda-feature {
    padding: 48px 6%;
  }

  .amanda-video-grid {
    grid-template-columns: 1fr;
    gap: 35px;
  }

  .amanda-intro {
    margin: 45px auto 55px;
  }

  .amanda-socials {
    flex-direction: column;
  }

  .amanda-social-link {
    justify-content: center;
  }
}

@media (max-width: 420px) {
  .newsletter form {
    flex-direction: column;
  }

  .newsletter button {
    padding: 14px;
  }

  .search-box button {
    padding: 0 14px;
  }
}
</style>
</head>

<body>

<!-- HEADER -->

<header>
  <div class="top-label">
    INDEPENDENT DIGITAL JOURNAL · EST. 2026
  </div>

  <div class="logo">
    MIDNIGHT <span>NEWS.</span>
  </div>

  <div class="tagline">
    Every hour has a story.
  </div>

  <div class="header-date" id="date"></div>
</header>

<!-- NAVIGATION -->

<nav>
  <a href="#home">HOME</a>
  <a href="#cover">COVER</a>
  <a href="#latest">LATEST</a>
  <a href="#amanda-king">TRAVEL</a>
  <a href="#search">SEARCH</a>
  <a href="#bookmarks">BOOKMARKS</a>
  <a href="#newsletter">NEWSLETTER</a>
</nav>

<!-- BREAKING STRIP -->

<div class="breaking">
  <div class="breaking-label">BREAKING</div>
  <div class="breaking-text">
    Your headlines will appear here.
  </div>
</div>

<!-- JAPAN CLOCK -->

<div class="clock-section">
  <div class="clock-label">TOKYO, JAPAN · JST</div>
  <div class="clock" id="clock">00:00:00</div>
  <div class="clock-note">JAPAN STANDARD TIME · UTC +9</div>
</div>

<main id="home">

  <!-- MAIN COVER -->

  <section id="cover">
    <div class="section-heading">
      <h2>The Cover Story</h2>
      <span></span>
    </div>

    <div class="cover">
      <div class="cover-small">THE MIDNIGHT EDITION</div>
      <h1>Your next cover<br>starts here.</h1>
      <p>YOUR IMAGE · YOUR STORY · YOUR WORLD</p>
      <div class="cover-line"></div>
    </div>
  </section>

  <!-- LATEST STORIES -->

  <section id="latest">
    <div class="section-heading">
      <h2>Latest Stories</h2>
      <span></span>
    </div>

    <div class="story-grid">

      <div class="story-card">
        <div class="story-number">01 / STORY</div>
        <h3>Story space 01</h3>
        <p>Your content will appear here.</p>
      </div>

      <div class="story-card">
        <div class="story-number">02 / STORY</div>
        <h3>Story space 02</h3>
        <p>Your content will appear here.</p>
      </div>

      <div class="story-card">
        <div class="story-number">03 / STORY</div>
        <h3>Story space 03</h3>
        <p>Your content will appear here.</p>
      </div>

    </div>
  </section>

  <!-- AMANDA KING: TRAVEL CREATOR SPOTLIGHT -->

  <section class="amanda-feature" id="amanda-king">

    <div class="amanda-kicker">
      Travel & Lifestyle — Creator Spotlight
    </div>

    <h2 class="amanda-title">
      My Favourite Travel Influencer —
      <em>Amanda King</em>
    </h2>

    <div class="amanda-subtitle">
      PEOPLE · PLACES · PERSPECTIVES
    </div>

    <!-- HERO IMAGE -->

    <div class="amanda-hero">
      <img
        src="https://images.squarespace-cdn.com/content/v1/67eb60db253c5c45656397d2/a6fde003-084c-44bf-bf31-79ff9d02c3a4/DSC01393.JPG"
        alt="Amanda King"
        loading="lazy"
      >
    </div>

    <div class="amanda-photo-caption">
      AMANDA KING — TRAVEL & CREATOR SPOTLIGHT
    </div>

    <!-- EXACT INTRODUCTION -->

    <div class="amanda-intro">
      <div class="amanda-intro-label">
        A PERSONAL NOTE
      </div>

      <p>Some creators inspire you to travel, explore and see the world differently. For me, Amanda King is one of those creators. Her travel videos, adventures and experiences make exploring the world even more exciting. That's why she is one of my favourite travel influencers.</p>
    </div>

    <div class="amanda-divider"></div>

    <!-- YOUTUBE VIDEOS -->

    <div>
      <h3 class="amanda-video-heading">
        TWO VIDEOS WORTH WATCHING
      </h3>

      <p class="amanda-video-note">
        TWO MOMENTS FROM AMANDA'S WORLD
      </p>

      <div class="amanda-video-grid">

        <!-- VIDEO ONE -->

        <a
          class="amanda-video-card"
          href="https://www.youtube.com/watch?v=kCeeTUSm4eo"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="amanda-thumbnail">
            <img
              src="https://img.youtube.com/vi/kCeeTUSm4eo/maxresdefault.jpg"
              alt="Amanda King's Shanghai travel vlog thumbnail"
              loading="lazy"
              onerror="this.src='https://img.youtube.com/vi/kCeeTUSm4eo/hqdefault.jpg'"
            >

            <div class="amanda-play">
              <svg viewBox="0 0 24 24" aria-hidden="true">
                <path d="M7 4L20 12L7 20Z"/>
              </svg>
            </div>
          </div>

          <div class="amanda-video-meta">
            <span>01</span>
            <span>TRAVEL VLOG</span>
          </div>

          <h4 class="amanda-video-title">
            Behind The Scenes as EMIRATES CABIN CREW - Things you DONT see as a Passenger - Shanghai Vlog
          </h4>

          <div class="amanda-video-open">
            WATCH ON YOUTUBE →
          </div>
        </a>

        <!-- VIDEO TWO -->

        <a
          class="amanda-video-card"
          href="https://www.youtube.com/watch?v=_-b3kdiSETI"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="amanda-thumbnail">
            <img
              src="https://img.youtube.com/vi/_-b3kdiSETI/maxresdefault.jpg"
              alt="Amanda King's second selected YouTube video thumbnail"
              loading="lazy"
              onerror="this.src='https://img.youtube.com/vi/_-b3kdiSETI/hqdefault.jpg'"
            >

            <div class="amanda-play">
              <svg viewBox="0 0 24 24" aria-hidden="true">
                <path d="M7 4L20 12L7 20Z"/>
              </svg>
            </div>
          </div>

          <div class="amanda-video-meta">
            <span>02</span>
            <span>SELECTED VIDEO</span>
          </div>

          <h4
            class="amanda-video-title"
            id="amanda-video-two-title"
          >
            Loading video title...
          </h4>

          <div class="amanda-video-open">
            WATCH ON YOUTUBE →
          </div>
        </a>

      </div>
    </div>

    <div class="amanda-divider"></div>

    <!-- SOCIAL MEDIA AT THE VERY END -->

    <div class="amanda-follow">

      <h3>FOLLOW AMANDA KING</h3>

      <div class="amanda-socials">

        <!-- INSTAGRAM -->

        <a
          class="amanda-social-link"
          href="https://www.instagram.com/its.amandaking/"
          target="_blank"
          rel="noopener noreferrer"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="3" y="3" width="18" height="18" rx="5"/>
            <circle cx="12" cy="12" r="4"/>
            <circle cx="17.5" cy="6.5" r=".7" fill="currentColor"/>
          </svg>

          <span>INSTAGRAM · @its.amandaking</span>
        </a>

        <!-- YOUTUBE -->

        <a
          class="amanda-social-link"
          href="https://www.youtube.com/@its.amandaking"
          target="_blank"
          rel="noopener noreferrer"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="2" y="5" width="20" height="14" rx="4"/>
            <path
              d="M10 9L16 12L10 15Z"
              fill="currentColor"
              stroke="none"
            />
          </svg>

          <span>YOUTUBE · @its.amandaking</span>
        </a>

      </div>
    </div>

  </section>

  <!-- SEARCH -->

  <section id="search">
    <div class="section-heading">
      <h2>Search the Journal</h2>
      <span></span>
    </div>

    <div class="search-box">
      <input
        type="text"
        id="searchInput"
        placeholder="Search the journal..."
      >

      <button onclick="searchJournal()">SEARCH</button>
    </div>

    <div class="search-message" id="searchMessage">
      Your journal search will be available when stories are added.
    </div>
  </section>

  <!-- BOOKMARKS -->

  <section id="bookmarks">
    <div class="section-heading">
      <h2>Your Bookmarks</h2>
      <span></span>
    </div>

    <div class="bookmark-area" id="bookmarkArea">
      Your saved stories will appear here.
    </div>
  </section>

  <!-- NEWSLETTER -->

  <section id="newsletter">
    <div class="newsletter">
      <h2>The Midnight Letter.</h2>

      <p>
        A little something from the world, delivered to your inbox.
      </p>

      <form onsubmit="subscribe(event)">
        <input
          type="email"
          placeholder="Your email address"
          required
        >

        <button type="submit">SUBSCRIBE</button>
      </form>

      <div id="newsletter-message"></div>
    </div>
  </section>

</main>

<!-- FOOTER -->

<footer>
  <div>MIDNIGHT <span>NEWS.</span></div>

  <p style="margin-top: 10px;">
    EVERY HOUR HAS A STORY.
  </p>

  <p style="margin-top: 15px;">
    © 2026 MIDNIGHT NEWS. ALL RIGHTS RESERVED.
  </p>
</footer>

<script>

/* JAPAN STANDARD TIME */

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


/* SECOND YOUTUBE VIDEO TITLE */

const secondVideoId = "_-b3kdiSETI";

const secondVideoTitle =
  document.getElementById("amanda-video-two-title");

fetch(
  "https://www.youtube.com/oembed?url=" +
  encodeURIComponent(
    "https://www.youtube.com/watch?v=" + secondVideoId
  ) +
  "&format=json"
)
.then(response => {
  if (!response.ok) {
    throw new Error("Video title unavailable");
  }

  return response.json();
})
.then(data => {
  secondVideoTitle.textContent = data.title;
})
.catch(() => {
  secondVideoTitle.textContent =
    "Watch Amanda's selected video on YouTube";
});


/* SEARCH PLACEHOLDER */

function searchJournal() {
  document.getElementById("searchMessage").textContent =
    "Your journal search will be activated when stories are added.";
}


/* BOOKMARKS */

function loadBookmarks() {
  const saved = JSON.parse(
    localStorage.getItem("midnightBookmarks") || "[]"
  );

  const area = document.getElementById("bookmarkArea");

  if (saved.length === 0) {
    area.textContent = "Your saved stories will appear here.";
  } else {
    area.innerHTML = saved.map(story =>
      `<p>${escapeHTML(story)}</p>`
    ).join("");
  }
}

function escapeHTML(value) {
  return String(value).replace(/[&<>"']/g, char => ({
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&#39;"
  })[char]);
}

loadBookmarks();


/* NEWSLETTER PLACEHOLDER */

function subscribe(event) {
  event.preventDefault();

  document.getElementById("newsletter-message").textContent =
    "Newsletter design is ready! A subscription service can be connected later.";
}

</script>

</body>
</html>
