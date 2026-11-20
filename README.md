
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MIDNIGHT NEWS — Every hour has a story.</title>

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #101110;
  --panel: #191c19;
  --green: #78d99a;
  --travel-accent: #b6c5a3;
  --text: #eeeee8;
  --muted: #999d96;
  --line: #303630;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
}

a {
  color: inherit;
  text-decoration: none;
}

.topline {
  padding: 12px 6%;
  border-bottom: 1px solid var(--line);
  display: flex;
  justify-content: space-between;
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
}

.header {
  text-align: center;
  padding: 35px 15px;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-size: clamp(36px, 6vw, 65px);
  letter-spacing: 5px;
  font-weight: 500;
}

.tagline {
  color: var(--green);
  font-family: 'Playfair Display', serif;
  font-style: italic;
  margin-top: 8px;
}

nav {
  display: flex;
  justify-content: center;
  gap: 35px;
  flex-wrap: wrap;
  padding: 17px 10px;
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}

nav a {
  color: #c6c9c1;
  font-size: 10px;
  letter-spacing: 2px;
  transition: .3s;
}

nav a:hover {
  color: var(--green);
}

.container {
  width: 88%;
  max-width: 1250px;
  margin: auto;
}

.section-label {
  font-size: 10px;
  letter-spacing: 3px;
  color: var(--green);
  margin-bottom: 23px;
  text-transform: uppercase;
}

.breaking {
  padding: 38px 0 15px;
}

.breaking-bar {
  background: var(--panel);
  padding: 16px 20px;
  border-left: 3px solid var(--green);
  display: flex;
  gap: 18px;
  flex-wrap: wrap;
  font-size: 12px;
}

.live { color: var(--green); }

/* AMANDA KING FEATURE */

.amanda {
  padding: 55px 0 75px;
  border-bottom: 1px solid var(--line);
}

.amanda-heading {
  text-align: center;
  margin-bottom: 35px;
}

.amanda-heading .eyebrow {
  color: var(--travel-accent);
  letter-spacing: 4px;
  font-size: 10px;
  margin-bottom: 15px;
}

.amanda-heading h1 {
  font-family: 'Playfair Display', serif;
  font-weight: 400;
  font-size: clamp(32px, 5vw, 57px);
  line-height: 1.2;
}

.amanda-heading h1 span {
  color: var(--green);
  font-style: italic;
}

.amanda-layout {
  display: grid;
  grid-template-columns: 1.05fr .95fr;
  gap: 55px;
  align-items: center;
}

.amanda-photo {
  width: 100%;
  height: 600px;
  object-fit: cover;
  object-position: center 35%;
  display: block;
}

.amanda-content .category {
  color: var(--green);
  letter-spacing: 3px;
  font-size: 10px;
  margin-bottom: 20px;
}

.amanda-content h2 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(31px, 4vw, 48px);
  font-weight: 400;
  line-height: 1.2;
  margin-bottom: 22px;
}

.amanda-content h2 em {
  color: var(--travel-accent);
}

.amanda-content p {
  color: #b0b3ac;
  font-size: 13px;
  line-height: 2.1;
  margin-bottom: 17px;
}

.amanda-content .highlight {
  color: var(--green);
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 19px;
  line-height: 1.7;
  margin: 25px 0;
}

.feature-meta {
  color: var(--muted);
  font-size: 9px;
  letter-spacing: 2px;
  margin-top: 30px;
}

/* VIDEOS */

.videos {
  padding: 65px 0;
  border-bottom: 1px solid var(--line);
}

.video-heading {
  font-family: 'Playfair Display', serif;
  font-size: 37px;
  font-weight: 400;
  margin-bottom: 12px;
}

.video-heading span {
  color: var(--green);
  font-style: italic;
}

.video-intro {
  color: var(--muted);
  font-size: 12px;
  margin-bottom: 30px;
}

.video-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.video-card img {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  display: block;
  transition: .4s;
}

.video-card:hover img {
  opacity: .75;
}

.video-card h3 {
  font-family: 'Playfair Display', serif;
  font-weight: 400;
  font-size: 23px;
  margin-top: 17px;
}

.video-card p {
  color: var(--muted);
  font-size: 11px;
  margin-top: 9px;
}

/* GENERAL NEWS */

.stories {
  padding: 65px 0;
}

.toolbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 30px;
}

.search {
  background: transparent;
  border: 1px solid var(--line);
  padding: 12px 15px;
  color: white;
  outline: none;
  width: 240px;
}

.search:focus {
  border-color: var(--green);
}

.bookmark-toggle {
  background: transparent;
  border: 1px solid var(--line);
  color: var(--green);
  padding: 12px 15px;
  cursor: pointer;
  font-size: 10px;
  letter-spacing: 1px;
}

.story-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.story {
  border-bottom: 1px solid var(--line);
  padding-bottom: 23px;
}

.story-image {
  height: 190px;
  background: linear-gradient(135deg,#303b31,#171a17);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--travel-accent);
  font-family: 'Playfair Display', serif;
  letter-spacing: 3px;
  margin-bottom: 18px;
}

.story .category {
  color: var(--green);
  font-size: 10px;
  letter-spacing: 2px;
}

.story h3 {
  font-family: 'Playfair Display', serif;
  font-size: 23px;
  font-weight: 400;
  margin: 13px 0;
  line-height: 1.4;
}

.story p {
  color: var(--muted);
  font-size: 12px;
  line-height: 1.8;
}

.story-footer {
  display: flex;
  justify-content: space-between;
  margin-top: 18px;
  color: var(--muted);
  font-size: 10px;
}

.save {
  background: transparent;
  border: none;
  color: var(--green);
  cursor: pointer;
  font-size: 18px;
}

.save.saved { color: white; }

.empty {
  display: none;
  color: var(--muted);
  padding: 25px;
  text-align: center;
}

/* NEWSLETTER */

.newsletter {
  background: var(--panel);
  text-align: center;
  padding: 65px 20px;
  margin: 20px 0 70px;
}

.newsletter h2 {
  font-family: 'Playfair Display', serif;
  font-size: 36px;
  font-weight: 400;
}

.newsletter h2 span { color: var(--green); }

.newsletter p {
  color: var(--muted);
  font-size: 12px;
  margin: 15px 0 25px;
}

.newsletter form {
  display: flex;
  max-width: 430px;
  margin: auto;
}

.newsletter input {
  flex: 1;
  min-width: 0;
  padding: 14px;
  background: transparent;
  border: 1px solid var(--line);
  color: white;
  outline: none;
}

.newsletter button {
  background: var(--green);
  color: #101510;
  border: none;
  padding: 0 20px;
  cursor: pointer;
  font-size: 10px;
  letter-spacing: 1px;
}

/* FOOTER */

footer {
  border-top: 1px solid var(--line);
  text-align: center;
  padding: 40px 15px;
  color: var(--muted);
  font-size: 10px;
  letter-spacing: 2px;
  line-height: 2.5;
}

footer strong {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 28px;
  font-weight: 400;
  color: var(--text);
  letter-spacing: 4px;
}

.socials {
  margin: 20px 0;
  display: flex;
  justify-content: center;
  gap: 25px;
  flex-wrap: wrap;
}

.socials a { color: var(--green); }

@media(max-width:800px) {
  .amanda-layout {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .amanda-photo { height: 500px; }

  .story-grid { grid-template-columns: repeat(2,1fr); }
}

@media(max-width:550px) {
  .story-grid, .video-grid { grid-template-columns: 1fr; }

  nav { gap: 17px; }

  .amanda-photo { height: 430px; }

  .newsletter form { flex-direction: column; gap: 10px; }

  .newsletter button { padding: 14px; }
}
</style>
</head>

<body>

<div class="topline">
  <span>INDEPENDENT DIGITAL JOURNAL</span>
  <span id="clock">JST --:--:--</span>
  <span>VOL. 001 — 2026</span>
</div>

<header class="header">
  <div class="logo">MIDNIGHT NEWS</div>
  <div class="tagline">Every hour has a story.</div>
</header>

<nav>
  <a href="#home">HOME</a>
  <a href="#amanda">FEATURE</a>
  <a href="#videos">VIDEOS</a>
  <a href="#world">WORLD</a>
  <a href="#culture">CULTURE</a>
  <a href="#newsletter">NEWSLETTER</a>
</nav>

<main class="container" id="home">

<section class="breaking">
  <div class="section-label">THE LATEST</div>
  <div class="breaking-bar">
    <span class="live">● EDITOR'S NOTE</span>
    <span>Welcome to Midnight News — every hour has a story.</span>
  </div>
</section>

<!-- AMANDA KING FEATURE -->

<section class="amanda" id="amanda">

  <div class="amanda-heading">
    <div class="eyebrow">TRAVEL & LIFESTYLE · SPECIAL FEATURE</div>
    <h1>MY FAVOURITE TRAVEL<br>
    INFLUENCER — <span>AMANDA KING</span></h1>
  </div>

  <div class="amanda-layout">

    <div>
      <img
        class="amanda-photo"
        src="image.png"
        alt="Amanda King at an outdoor event"
      >
    </div>

    <div class="amanda-content">

      <div class="category">THE PEOPLE WE ADMIRE · 001</div>

      <h2>Some journeys are worth following.</h2>

      <p>
        Travel is more than visiting new places. It is about
        discovering different perspectives, collecting memories
        and finding inspiration in the world around us.
      </p>

      <p>
        Amanda King is a travel influencer whose videos and
        adventures make exploring the world feel exciting.
        Her content celebrates the experiences, destinations
        and moments that make travelling so memorable.
      </p>

      <div class="highlight">
        "A little inspiration can make the whole world feel closer."
      </div>

      <p>
        This feature is dedicated to the creator whose travel
        adventures make us want to see a little more of the world.
      </p>

      <div class="feature-meta">
        MIDNIGHT EDITORIAL · TRAVEL & LIFESTYLE
      </div>

    </div>
  </div>

</section>

<!-- TWO VIDEOS -->

<section class="videos" id="videos">

  <div class="section-label">THE WATCH LIST</div>

  <h2 class="video-heading">
    TWO VIDEOS <span>WORTH WATCHING</span>
  </h2>

  <p class="video-intro">
    A little more of Amanda's world, one video at a time.
  </p>

  <div class="video-grid">

    <a class="video-card"
       href="https://www.youtube.com/watch?v=kCeeTUSm4eo"
       target="_blank" rel="noopener">

      <img
        src="https://img.youtube.com/vi/kCeeTUSm4eo/maxresdefault.jpg"
        onerror="this.src='https://img.youtube.com/vi/kCeeTUSm4eo/hqdefault.jpg'"
        alt="First Amanda King video thumbnail">

      <h3>Video No. 01</h3>
      <p>WATCH ON YOUTUBE ↗</p>
    </a>

    <a class="video-card"
       href="https://www.youtube.com/watch?v=_-b3kdiSETI"
       target="_blank" rel="noopener">

      <img
        src="https://img.youtube.com/vi/_-b3kdiSETI/maxresdefault.jpg"
        onerror="this.src='https://img.youtube.com/vi/_-b3kdiSETI/hqdefault.jpg'"
        alt="Second Amanda King video thumbnail">

      <h3>Video No. 02</h3>
      <p>WATCH ON YOUTUBE ↗</p>
    </a>

  </div>
</section>

<!-- JOURNAL -->

<section class="stories" id="world">

  <div class="toolbar">
    <div>
      <div class="section-label" style="margin:0">THE JOURNAL</div>
    </div>

    <div style="display:flex;gap:10px;flex-wrap:wrap">
      <input
        class="search"
        id="search"
        placeholder="Search stories..."
      >

      <button class="bookmark-toggle" id="showBookmarks">
        ♡ BOOKMARKS
      </button>
    </div>
  </div>

  <div class="story-grid" id="storyGrid">

    <article class="story" data-category="world">
      <div class="story-image">WORLD</div>
      <div class="category">WORLD</div>
      <h3>A changing world and the stories behind it.</h3>
      <p>Explore events, conversations and developments shaping our global landscape.</p>
      <div class="story-footer">
        <span>WORLD DESK</span>
        <button class="save">♡</button>
      </div>
    </article>

    <article class="story" id="culture" data-category="culture">
      <div class="story-image">CULTURE</div>
      <div class="category">CULTURE</div>
      <h3>The art of seeing the world differently.</h3>
      <p>Art, creativity, entertainment and the people changing cultural conversations.</p>
      <div class="story-footer">
        <span>CULTURE DESK</span>
        <button class="save">♡</button>
      </div>
    </article>

    <article class="story" data-category="lifestyle">
      <div class="story-image">LIFESTYLE</div>
      <div class="category">LIFESTYLE</div>
      <h3>Finding meaning in the everyday.</h3>
      <p>Ideas, inspiration, travel and the little things that make life interesting.</p>
      <div class="story-footer">
        <span>LIFESTYLE DESK</span>
        <button class="save">♡</button>
      </div>
    </article>

    <article class="story" data-category="technology">
      <div class="story-image">TECHNOLOGY</div>
      <div class="category">TECHNOLOGY</div>
      <h3>Tomorrow is already taking shape.</h3>
      <p>Discover innovations and digital ideas transforming the future.</p>
      <div class="story-footer">
        <span>TECH DESK</span>
        <button class="save">♡</button>
      </div>
    </article>

    <article class="story" data-category="world">
      <div class="story-image">PERSPECTIVE</div>
      <div class="category">PERSPECTIVE</div>
      <h3>Beyond the headlines.</h3>
      <p>Thoughtful commentary and context behind the conversations that matter.</p>
      <div class="story-footer">
        <span>OPINION DESK</span>
        <button class="save">♡</button>
      </div>
    </article>

    <article class="story" data-category="culture">
      <div class="story-image">THE EDIT</div>
      <div class="category">THE EDIT</div>
      <h3>Stories worth slowing down for.</h3>
      <p>A carefully selected collection of discoveries and interesting reads.</p>
      <div class="story-footer">
        <span>THE EDITORS</span>
        <button class="save">♡</button>
      </div>
    </article>

  </div>

  <p class="empty" id="empty">No stories found.</p>

</section>

<!-- NEWSLETTER -->

<section class="newsletter" id="newsletter">

  <div class="section-label">THE MIDNIGHT LETTER</div>

  <h2>A little news, <span>a little perspective.</span></h2>

  <p>Get the stories worth knowing, delivered to your inbox.</p>

  <form id="newsletterForm">
    <input type="email" placeholder="Your email address" required>
    <button type="submit">SUBSCRIBE →</button>
  </form>

  <p id="newsletterMessage"></p>

</section>

</main>

<footer>

  <strong>MIDNIGHT NEWS</strong>

  EVERY HOUR HAS A STORY.

  <div class="socials">
    <a href="https://www.instagram.com/" target="_blank">INSTAGRAM ↗</a>
    <a href="https://www.youtube.com/" target="_blank">YOUTUBE ↗</a>
    <a href="https://www.pinterest.com/" target="_blank">PINTEREST ↗</a>
  </div>

  © 2026 MIDNIGHT NEWS · INDEPENDENT DIGITAL JOURNAL

</footer>

<script>

// JAPAN STANDARD TIME

function updateClock() {
  const now = new Date();

  document.getElementById("clock").textContent =
    "JST " + new Intl.DateTimeFormat("en-GB", {
      timeZone: "Asia/Tokyo",
      hour: "2-digit",
      minute: "2-digit",
      second: "2-digit",
      hour12: false
    }).format(now);
}

updateClock();
setInterval(updateClock, 1000);


// SEARCH

const search = document.getElementById("search");
const stories = [...document.querySelectorAll(".story")];
const empty = document.getElementById("empty");

let bookmarksOnly = false;

function filterStories() {

  let visible = 0;
  const term = search.value.toLowerCase();

  stories.forEach(story => {

    const matchesText =
      story.innerText.toLowerCase().includes(term);

    const matchesBookmark =
      !bookmarksOnly ||
      story.querySelector(".save").classList.contains("saved");

    const show = matchesText && matchesBookmark;

    story.style.display = show ? "" : "none";

    if (show) visible++;
  });

  empty.style.display = visible ? "none" : "block";
}

search.addEventListener("input", filterStories);


// BOOKMARKS

document.querySelectorAll(".save").forEach(button => {

  button.addEventListener("click", () => {

    button.classList.toggle("saved");

    button.textContent =
      button.classList.contains("saved") ? "♥" : "♡";

    filterStories();

  });

});

document.getElementById("showBookmarks")
.addEventListener("click", () => {

  bookmarksOnly = !bookmarksOnly;

  document.getElementById("showBookmarks").textContent =
    bookmarksOnly ? "← ALL STORIES" : "♡ BOOKMARKS";

  filterStories();

});


// NEWSLETTER DEMO

document.getElementById("newsletterForm")
.addEventListener("submit", event => {

  event.preventDefault();

  document.getElementById("newsletterMessage").textContent =
    "Thank you for your interest in The Midnight Letter!";

  event.target.reset();

});

</script>

</body>
</html>
