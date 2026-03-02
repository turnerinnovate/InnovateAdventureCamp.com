```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Innovate Adventure Camp | Summer Reengineered</title>
  <meta name="description" content="Innovate Adventure Camp: 9 epic summer weeks inside the dome. Monday-Friday sessions. Registration open now." />
  <style>
    :root {
      --bg: #07091f;
      --bg-soft: #101535;
      --panel: rgba(14, 18, 46, 0.78);
      --panel-strong: rgba(9, 12, 34, 0.92);
      --line: rgba(255, 255, 255, 0.18);
      --text: #f3f6ff;
      --muted: #c8cdef;
      --gold: #ffc84f;
      --cyan: #3fe3ff;
      --pink: #ff65c9;
      --violet: #7b57ff;
      --ok: #6cf3d2;
      --shadow: 0 24px 52px rgba(2, 4, 18, 0.5);
      --radius: 20px;
    }

    * { box-sizing: border-box; }

    html, body {
      margin: 0;
      padding: 0;
      color: var(--text);
      background: radial-gradient(circle at 12% 10%, rgba(255, 101, 201, 0.22), transparent 35%),
        radial-gradient(circle at 88% 16%, rgba(63, 227, 255, 0.2), transparent 38%),
        radial-gradient(circle at 50% 84%, rgba(123, 87, 255, 0.3), transparent 48%),
        linear-gradient(160deg, var(--bg) 0%, #090d2a 42%, #060814 100%);
      font-family: "Avenir Next", "Montserrat", "Segoe UI", sans-serif;
      min-height: 100%;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: -1;
      background:
        radial-gradient(circle at 20% 30%, rgba(255, 255, 255, 0.14) 1px, transparent 1px),
        radial-gradient(circle at 80% 70%, rgba(255, 255, 255, 0.14) 1px, transparent 1px);
      background-size: 150px 150px, 210px 210px;
      opacity: 0.4;
    }

    .wrap {
      width: min(1180px, 92vw);
      margin: 0 auto;
      padding: 26px 0 60px;
    }

    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 14px;
      margin-bottom: 16px;
      padding: 10px 14px;
      border: 1px solid var(--line);
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.04);
      backdrop-filter: blur(6px);
    }

    .brand {
      font-weight: 900;
      letter-spacing: 0.02em;
      text-transform: uppercase;
      color: #f7f8ff;
      text-decoration: none;
    }

    .brand span {
      color: var(--gold);
    }

    .nav-links {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .nav-links a {
      color: var(--muted);
      text-decoration: none;
      font-weight: 700;
      font-size: 0.9rem;
      padding: 8px 10px;
      border-radius: 10px;
      border: 1px solid transparent;
    }

    .nav-links a:hover {
      color: var(--text);
      border-color: var(--line);
      background: rgba(255, 255, 255, 0.04);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border: 0;
      border-radius: 12px;
      padding: 13px 18px;
      text-decoration: none;
      text-transform: uppercase;
      letter-spacing: 0.03em;
      font-weight: 900;
      cursor: pointer;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .btn:hover { transform: translateY(-2px); }

    .btn-primary {
      color: #190f03;
      background: linear-gradient(130deg, #ffd963, #ffbe3f 52%, #ff9a00);
      box-shadow: 0 16px 30px rgba(255, 174, 35, 0.35);
    }

    .btn-ghost {
      color: var(--text);
      border: 1px solid var(--line);
      background: rgba(255, 255, 255, 0.07);
    }

    .hero {
      border: 1px solid var(--line);
      border-radius: 28px;
      padding: 46px 26px;
      background:
        radial-gradient(circle at 86% 14%, rgba(63, 227, 255, 0.22), transparent 35%),
        radial-gradient(circle at 14% 72%, rgba(255, 101, 201, 0.25), transparent 44%),
        linear-gradient(140deg, rgba(15, 19, 53, 0.93), rgba(8, 11, 31, 0.92));
      box-shadow: var(--shadow);
      overflow: hidden;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 480px;
      height: 480px;
      right: -180px;
      top: -220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(123, 87, 255, 0.34), transparent 62%);
      pointer-events: none;
    }

    .eyebrow {
      display: inline-block;
      font-size: 0.72rem;
      text-transform: uppercase;
      font-weight: 800;
      letter-spacing: 0.08em;
      color: #ecf0ff;
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid var(--line);
      border-radius: 999px;
      padding: 7px 12px;
    }

    h1 {
      margin: 16px 0 10px;
      font-size: clamp(2.1rem, 5.6vw, 4.6rem);
      line-height: 0.94;
      letter-spacing: -0.03em;
      text-transform: uppercase;
      max-width: 10ch;
    }

    .shine {
      background: linear-gradient(92deg, #fff 0%, #ffe6a4 30%, #ffcb5a 60%, #ff9a00 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 0 6px 22px rgba(255, 182, 38, 0.28);
    }

    .lead {
      max-width: 62ch;
      color: var(--muted);
      font-size: clamp(1rem, 1.35vw, 1.18rem);
      line-height: 1.58;
      margin-bottom: 20px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 16px;
    }

    .meta {
      color: #dbe0ff;
      font-weight: 700;
      font-size: 0.92rem;
      line-height: 1.45;
    }

    .stats {
      margin-top: 18px;
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 10px;
    }

    .stat {
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.08);
      padding: 12px;
      text-align: center;
    }

    .stat strong {
      display: block;
      font-size: 1.35rem;
      color: var(--gold);
      line-height: 1;
      margin-bottom: 4px;
    }

    .section {
      margin-top: 22px;
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 26px 20px;
      background: var(--panel);
      box-shadow: var(--shadow);
    }

    h2 {
      margin: 0 0 10px;
      font-size: clamp(1.35rem, 3vw, 2rem);
      text-transform: uppercase;
      letter-spacing: 0.01em;
    }

    .section p {
      margin: 0;
      color: var(--muted);
      line-height: 1.55;
    }

    .pill-grid {
      margin-top: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .pill {
      padding: 8px 12px;
      border-radius: 999px;
      border: 1px solid rgba(63, 227, 255, 0.45);
      background: rgba(63, 227, 255, 0.14);
      font-weight: 700;
      font-size: 0.9rem;
    }

    .themes {
      margin-top: 14px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 10px;
    }

    .theme {
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.05);
      padding: 12px;
    }

    .theme h3 {
      margin: 0 0 6px;
      text-transform: uppercase;
      font-size: 0.98rem;
      color: #f0f3ff;
      letter-spacing: 0.03em;
    }

    .theme p {
      margin: 0;
      color: var(--muted);
      font-size: 0.92rem;
    }

    .schedule-grid {
      margin-top: 14px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 10px;
    }

    .week {
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.06);
      padding: 11px;
    }

    .week strong {
      color: #ffe59d;
      display: block;
      margin-bottom: 4px;
    }

    .break {
      margin-top: 10px;
      border: 1px solid rgba(255, 101, 201, 0.5);
      border-radius: 10px;
      background: rgba(255, 101, 201, 0.16);
      padding: 10px 12px;
      color: #ffd1ef;
      font-weight: 800;
    }

    .gallery {
      margin-top: 14px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 10px;
    }

    .shot {
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--line);
      background: var(--panel-strong);
    }

    .shot img {
      display: block;
      width: 100%;
      height: 230px;
      object-fit: cover;
      background: linear-gradient(135deg, rgba(123, 87, 255, 0.4), rgba(63, 227, 255, 0.25));
    }

    .shot figcaption {
      margin: 0;
      padding: 10px;
      color: #dbe1ff;
      font-size: 0.87rem;
      border-top: 1px solid var(--line);
    }

    .register-wrap {
      margin-top: 14px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }

    .panel {
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.05);
      padding: 14px;
    }

    .panel h3 {
      margin: 0 0 8px;
      text-transform: uppercase;
      font-size: 0.95rem;
      letter-spacing: 0.03em;
    }

    .stack {
      display: grid;
      gap: 10px;
    }

    label {
      display: grid;
      gap: 5px;
      font-weight: 700;
      font-size: 0.89rem;
      color: #e2e7ff;
    }

    input,
    textarea,
    select {
      width: 100%;
      border: 1px solid var(--line);
      border-radius: 10px;
      padding: 10px 11px;
      font: inherit;
      color: var(--text);
      background: rgba(255, 255, 255, 0.08);
    }

    input:focus,
    textarea:focus,
    select:focus {
      outline: 2px solid rgba(63, 227, 255, 0.55);
      outline-offset: 1px;
    }

    .weeks {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 6px;
      border: 1px solid var(--line);
      border-radius: 10px;
      background: rgba(255, 255, 255, 0.04);
      padding: 10px;
    }

    .check {
      display: flex;
      gap: 8px;
      align-items: center;
      font-size: 0.86rem;
      color: #e4e8ff;
    }

    .check input {
      width: auto;
      margin: 0;
      accent-color: var(--cyan);
    }

    .fine {
      margin: 0;
      color: #bfc6ec;
      font-size: 0.8rem;
      line-height: 1.45;
    }

    .actions {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .notice {
      display: none;
      margin-top: 8px;
      border: 1px solid rgba(108, 243, 210, 0.55);
      border-radius: 10px;
      background: rgba(108, 243, 210, 0.14);
      color: #ddfff6;
      font-weight: 800;
      padding: 10px;
      font-size: 0.9rem;
    }

    .notice.show { display: block; }

    .footer {
      margin-top: 14px;
      text-align: center;
      color: #b8bfe9;
      font-size: 0.88rem;
    }

    @media (max-width: 980px) {
      .register-wrap { grid-template-columns: 1fr; }
      .stats { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    }

    @media (max-width: 620px) {
      .wrap { width: min(1180px, 94vw); }
      .hero { padding: 34px 16px; }
      .section { padding: 20px 14px; }
      .weeks { grid-template-columns: 1fr; }
      .stats { grid-template-columns: 1fr 1fr; }
      .nav { flex-direction: column; align-items: stretch; }
      .nav-links { justify-content: center; }
      .nav .btn { width: 100%; }
      .hero-actions .btn { width: 100%; }
    }
  </style>
</head>
<body>
  <main class="wrap">
    <nav class="nav">
      <a class="brand" href="#top">Innovate <span>Adventure Camp</span></a>
      <div class="nav-links">
        <a href="#why">Why Us</a>
        <a href="#schedule">Schedule</a>
        <a href="#gallery">Creative</a>
        <a href="#register">Register</a>
      </div>
      <a class="btn btn-primary" href="#register">Enroll Now</a>
    </nav>

    <header id="top" class="hero">
      <span class="eyebrow">Summer 2026 Registration Open</span>
      <h1>Summer <span class="shine">Reengineered</span></h1>
      <p class="lead">This is not normal camp. This is nine high-energy weeks inside the dome where kids run, play, compete, build, and level up through games, experiments, team challenges, and creator projects.</p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="#register">Register Interest</a>
        <a class="btn btn-ghost" href="https://innovateadventurecamp.com" target="_blank" rel="noreferrer">Full Registration Site</a>
      </div>
      <div class="meta">Monday-Friday sessions | No camp July 13-17, 2026 | Ages 5-14 | [City, State]</div>
      <div class="stats">
        <div class="stat"><strong>9</strong>Epic Weeks</div>
        <div class="stat"><strong>1</strong>Massive Dome</div>
        <div class="stat"><strong>5-14</strong>Camp Ages</div>
        <div class="stat"><strong>Mon-Fri</strong>All Summer</div>
      </div>
    </header>

    <section id="why" class="section">
      <h2>Built To Be Untouchable</h2>
      <p>Innovate Adventure Camp combines sports energy, STEM excitement, and creator confidence into one experience parents can trust and kids cannot wait to return to each morning.</p>
      <div class="pill-grid">
        <span class="pill">One giant indoor dome</span>
        <span class="pill">New challenge momentum every week</span>
        <span class="pill">Structured groups and safety-first staff</span>
        <span class="pill">Confidence + teamwork outcomes</span>
      </div>
      <div class="themes">
        <article class="theme">
          <h3>Action Games</h3>
          <p>Athletic competitions, relay formats, and fast team missions with inclusive coaching.</p>
        </article>
        <article class="theme">
          <h3>Science Experiments</h3>
          <p>Hands-on experiments designed for wow moments and practical curiosity.</p>
        </article>
        <article class="theme">
          <h3>Team Challenges</h3>
          <p>Collaborative events that train leadership, communication, and resilience.</p>
        </article>
        <article class="theme">
          <h3>DIY Creator Lab</h3>
          <p>Build sessions where campers design, test, and present their projects.</p>
        </article>
      </div>
    </section>

    <section id="schedule" class="section">
      <h2>2026 Camp Schedule</h2>
      <p>Exact session dates for summer 2026. All weeks run Monday-Friday.</p>
      <div class="schedule-grid">
        <article class="week"><strong>Week 1</strong>June 29-July 3</article>
        <article class="week"><strong>Week 2</strong>July 6-10</article>
        <article class="week"><strong>Week 3</strong>July 20-24</article>
        <article class="week"><strong>Week 4</strong>July 27-31</article>
        <article class="week"><strong>Week 5</strong>August 3-7</article>
        <article class="week"><strong>Week 6</strong>August 10-14</article>
        <article class="week"><strong>Week 7</strong>August 17-21</article>
        <article class="week"><strong>Week 8</strong>August 24-28</article>
        <article class="week"><strong>Week 9</strong>August 31-September 4</article>
      </div>
      <div class="break">No Camp Week: July 13-17, 2026</div>
    </section>

    <section id="gallery" class="section">
      <h2>Creative Gallery</h2>
      <p>Drop your final ad renders into the assets folder to instantly update this section.</p>
      <div class="gallery">
        <figure class="shot">
          <img src="./assets/ad-1.jpg" alt="Innovate ad concept 1" loading="lazy" />
          <figcaption>Hero Poster</figcaption>
        </figure>
        <figure class="shot">
          <img src="./assets/ad-2.jpg" alt="Innovate ad concept 2" loading="lazy" />
          <figcaption>Primary Conversion Visual</figcaption>
        </figure>
        <figure class="shot">
          <img src="./assets/ad-3.jpg" alt="Innovate ad concept 3" loading="lazy" />
          <figcaption>Social Carousel</figcaption>
        </figure>
        <figure class="shot">
          <img src="./assets/ad-4.jpg" alt="Innovate ad concept 4" loading="lazy" />
          <figcaption>Legendary Campaign</figcaption>
        </figure>
        <figure class="shot">
          <img src="./assets/ad-5.jpg" alt="Innovate ad concept 5" loading="lazy" />
          <figcaption>Not Normal Camp</figcaption>
        </figure>
        <figure class="shot">
          <img src="./assets/ad-6.jpg" alt="Innovate ad concept 6" loading="lazy" />
          <figcaption>Bigger Space Message</figcaption>
        </figure>
      </div>
    </section>

    <section id="register" class="section">
      <h2>Register Interest</h2>
      <p>Submit this quick form and the Innovate team will contact you to confirm placement and payment details.</p>
      <div class="register-wrap">
        <form id="interestForm" class="panel stack" novalidate>
          <h3>Parent + Camper Details</h3>
          <label>Parent/Guardian Name
            <input type="text" name="parentName" required />
          </label>
          <label>Email
            <input type="email" name="email" required />
          </label>
          <label>Phone
            <input type="tel" name="phone" required />
          </label>
          <label>Camper Name
            <input type="text" name="camperName" required />
          </label>
          <label>Camper Age
            <select name="camperAge" required>
              <option value="">Select age</option>
              <option>5</option><option>6</option><option>7</option><option>8</option><option>9</option>
              <option>10</option><option>11</option><option>12</option><option>13</option><option>14</option>
            </select>
          </label>
          <label>Notes (allergies, support needs, pickup info)
            <textarea name="notes" rows="4" placeholder="Share any important details."></textarea>
          </label>
        </form>

        <div class="panel stack">
          <h3>Select Weeks</h3>
          <div class="weeks" id="weekPicker">
            <label class="check"><input type="checkbox" value="Week 1: Jun 29-Jul 3" />Week 1: Jun 29-Jul 3</label>
            <label class="check"><input type="checkbox" value="Week 2: Jul 6-10" />Week 2: Jul 6-10</label>
            <label class="check"><input type="checkbox" value="Week 3: Jul 20-24" />Week 3: Jul 20-24</label>
            <label class="check"><input type="checkbox" value="Week 4: Jul 27-31" />Week 4: Jul 27-31</label>
            <label class="check"><input type="checkbox" value="Week 5: Aug 3-7" />Week 5: Aug 3-7</label>
            <label class="check"><input type="checkbox" value="Week 6: Aug 10-14" />Week 6: Aug 10-14</label>
            <label class="check"><input type="checkbox" value="Week 7: Aug 17-21" />Week 7: Aug 17-21</label>
            <label class="check"><input type="checkbox" value="Week 8: Aug 24-28" />Week 8: Aug 24-28</label>
            <label class="check"><input type="checkbox" value="Week 9: Aug 31-Sep 4" />Week 9: Aug 31-Sep 4</label>
          </div>
          <p class="fine">By submitting, you agree to be contacted by Innovate Adventure Camp about enrollment.</p>
          <div class="actions">
            <button id="submitInterest" class="btn btn-primary" type="button">Submit Interest</button>
            <a class="btn btn-ghost" href="https://innovateadventurecamp.com" target="_blank" rel="noreferrer">Open Full Registration</a>
          </div>
          <p id="notice" class="notice">Thanks. Your request has been captured.</p>
        </div>
      </div>
    </section>

    <p class="footer">Innovate Adventure Camp | Registration Open Now | Monday-Friday Sessions</p>
  </main>

  <script>
    (function () {
      const form = document.getElementById("interestForm");
      const picker = document.getElementById("weekPicker");
      const submit = document.getElementById("submitInterest");
      const notice = document.getElementById("notice");

      function selectedWeeks() {
        return Array.from(picker.querySelectorAll('input[type="checkbox"]:checked')).map((el) => el.value);
      }

      function isValid() {
        return form.reportValidity() && selectedWeeks().length > 0;
      }

      submit.addEventListener("click", function () {
        if (!isValid()) {
          if (selectedWeeks().length === 0) {
            alert("Please select at least one camp week.");
          }
          return;
        }

        const payload = {
          submittedAt: new Date().toISOString(),
          parentName: form.elements.parentName.value.trim(),
          email: form.elements.email.value.trim(),
          phone: form.elements.phone.value.trim(),
          camperName: form.elements.camperName.value.trim(),
          camperAge: form.elements.camperAge.value,
          notes: form.elements.notes.value.trim(),
          weeks: selectedWeeks()
        };

        localStorage.setItem("innovateCampLead", JSON.stringify(payload));
        notice.classList.add("show");
        form.reset();
        picker.querySelectorAll('input[type="checkbox"]').forEach((c) => {
          c.checked = false;
        });
      });
    })();
  </script>
</body>
</html>
```
