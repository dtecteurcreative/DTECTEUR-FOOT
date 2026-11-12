<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101510">
<title>DTECTEUR FOOT | Football en Direct</title>

<style>
:root {
  --bg:#101510;
  --card:#1a211b;
  --green:#00d66b;
  --white:#ffffff;
  --muted:#a5b1a8;
  --border:#2a352c;
}

* { box-sizing:border-box; margin:0; padding:0; }

body {
  background:var(--bg);
  color:var(--white);
  font-family:Arial,sans-serif;
  line-height:1.5;
}

a { color:inherit; text-decoration:none; }

header {
  padding:17px 5%;
  display:flex;
  align-items:center;
  justify-content:space-between;
  border-bottom:1px solid var(--border);
  position:sticky;
  top:0;
  z-index:10;
  background:#101510;
}

.logo {
  font-size:21px;
  font-weight:900;
  letter-spacing:-1px;
}

.logo span { color:var(--green); }

nav {
  display:flex;
  gap:20px;
}

nav a {
  color:var(--muted);
  font-size:13px;
  font-weight:bold;
}

nav a:hover { color:var(--green); }

.hero {
  padding:65px 6%;
  background:linear-gradient(110deg,#14251a,#101510 75%);
  border-bottom:1px solid var(--border);
}

.tag {
  color:var(--green);
  font-size:12px;
  font-weight:bold;
  letter-spacing:2px;
}

.hero h1 {
  font-size:clamp(32px,6vw,58px);
  line-height:1.12;
  margin:15px 0;
}

.hero h1 span { color:var(--green); }

.hero p {
  color:var(--muted);
  max-width:500px;
  font-size:15px;
}

.button {
  display:inline-block;
  background:var(--green);
  color:#07130b;
  padding:12px 20px;
  border-radius:6px;
  font-weight:bold;
  margin-top:22px;
}

.container {
  width:90%;
  max-width:1150px;
  margin:35px auto;
}

.section-title {
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:18px;
}

.section-title h2 { font-size:21px; }

.section-title span {
  color:var(--green);
  font-size:12px;
  font-weight:bold;
}

.ad {
  border:1px dashed #536052;
  background:#151c16;
  padding:20px;
  text-align:center;
  border-radius:8px;
  color:var(--muted);
  margin:25px 0;
  font-size:12px;
}

.ad strong {
  display:block;
  color:var(--green);
  margin-bottom:5px;
}

.live-card {
  background:linear-gradient(120deg,#203a29,#172019);
  border:1px solid #31583d;
  border-radius:12px;
  padding:25px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:15px;
  flex-wrap:wrap;
}

.live-label {
  color:var(--green);
  font-weight:bold;
  font-size:12px;
}

.live-card h3 { margin:9px 0; }

.live-card p {
  color:var(--muted);
  font-size:13px;
}

.live-link {
  background:var(--green);
  color:#06150a;
  padding:11px 17px;
  border-radius:6px;
  font-weight:bold;
  font-size:13px;
}

.search {
  width:100%;
  background:var(--card);
  border:1px solid var(--border);
  padding:14px;
  border-radius:7px;
  color:white;
  outline:none;
  margin-bottom:15px;
  font-size:15px;
}

.filters {
  display:flex;
  gap:9px;
  overflow-x:auto;
  margin-bottom:20px;
}

.filters button {
  background:var(--card);
  color:white;
  border:1px solid var(--border);
  padding:10px 17px;
  border-radius:6px;
  white-space:nowrap;
  cursor:pointer;
}

.filters button.active {
  background:var(--green);
  color:#07130b;
  font-weight:bold;
}

.matches {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
  gap:15px;
}

.match {
  background:var(--card);
  padding:18px;
  border:1px solid var(--border);
  border-radius:9px;
}

.league {
  color:var(--green);
  font-size:11px;
  font-weight:bold;
  margin-bottom:15px;
}

.teams {
  display:flex;
  align-items:center;
  justify-content:space-between;
  text-align:center;
  gap:8px;
}

.team {
  flex:1;
  font-weight:bold;
  font-size:13px;
}

.team-icon {
  display:block;
  font-size:27px;
  margin-bottom:5px;
}

.vs {
  color:var(--muted);
  font-size:12px;
}

.match-time {
  border-top:1px solid var(--border);
  margin-top:15px;
  padding-top:12px;
  text-align:center;
  color:var(--muted);
  font-size:12px;
}

.score {
  color:var(--green);
  font-weight:bold;
  font-size:17px;
}

.empty {
  color:var(--muted);
  padding:20px;
  text-align:center;
  grid-column:1/-1;
}

.news-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:15px;
}

.news {
  background:var(--card);
  border:1px solid var(--border);
  padding:20px;
  border-radius:8px;
}

.news h3 { margin:10px 0; font-size:16px; }

.news p { color:var(--muted); font-size:13px; }

.news small { color:var(--green); }

.standings {
  width:100%;
  border-collapse:collapse;
  background:var(--card);
  border-radius:8px;
  overflow:hidden;
}

.standings th,.standings td {
  padding:13px 10px;
  border-bottom:1px solid var(--border);
  text-align:left;
  font-size:13px;
}

.standings th { color:var(--green); }

footer {
  border-top:1px solid var(--border);
  padding:35px 5%;
  text-align:center;
  color:var(--muted);
  font-size:13px;
  margin-top:50px;
}

footer strong { color:var(--green); }

@media(max-width:600px) {
  header { padding:14px 4%; }
  .logo { font-size:17px; }
  nav { gap:12px; }
  nav a { font-size:11px; }
  .hero { padding:45px 5%; }
  .container { width:92%; }
  .live-card { padding:18px; }
}
</style>
</head>

<body>

<header>
  <a href="#" class="logo">DTECTEUR <span>FOOT</span></a>

  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#direct">Direct</a>
    <a href="#matchs">Matchs</a>
    <a href="#resultats">Résultats</a>
  </nav>
</header>

<section class="hero" id="accueil">
  <div class="tag">LE FOOTBALL SANS FRONTIÈRES</div>

  <h1>Vivez le football<br><span>autrement.</span></h1>

  <p>
    Retrouvez les matchs, résultats, actualités et
    liens vers les diffusions officielles.
    Toute votre passion du football au même endroit.
  </p>

  <a href="#matchs" class="button">Explorer les matchs →</a>
</section>

<div class="container">

  <div class="ad">
    <strong>ESPACE PUBLICITAIRE</strong>
    Votre marque peut apparaître ici.
    <br>Contactez DTECTEUR FOOT pour devenir sponsor.
  </div>

  <section id="direct">
    <div class="section-title">
      <h2>🔴 Football en direct</h2>
      <span>LIVE</span>
    </div>

    <div class="live-card">
      <div>
        <div class="live-label">● DIFFUSIONS OFFICIELLES</div>
        <h3>Ne manquez aucun grand match</h3>
        <p>Retrouvez les compétitions disponibles gratuitement.</p>
      </div>

      <a class="live-link"
         href="https://www.plus.fifa.com/"
         target="_blank" rel="noopener">
         REGARDER →
      </a>
    </div>
  </section>

  <section id="matchs" style="margin-top:40px">

    <div class="section-title">
      <h2>⚽ Programme des matchs</h2>
      <span>FOOTBALL</span>
    </div>

    <input
      type="search"
      class="search"
      id="search"
      placeholder="Rechercher une équipe ou compétition..."
    >

    <div class="filters">
      <button class="active" data-filter="all">Tous</button>
      <button data-filter="Premier League">Premier League</button>
      <button data-filter="La Liga">La Liga</button>
      <button data-filter="Ligue 1">Ligue 1</button>
      <button data-filter="Champions League">Champions League</button>
    </div>

    <div class="matches" id="matches">

      <article class="match" data-league="Premier League">
        <div class="league">PREMIER LEAGUE</div>
        <div class="teams">
          <div class="team">
            <span class="team-icon">🔴</span>
            Arsenal
          </div>
          <div class="vs">VS</div>
          <div class="team">
            <span class="team-icon">🔵</span>
            Chelsea
          </div>
        </div>
        <div class="match-time">Données de démonstration</div>
      </article>

      <article class="match" data-league="La Liga">
        <div class="league">LA LIGA</div>
        <div class="teams">
          <div class="team">
            <span class="team-icon">⚪</span>
            Real Madrid
          </div>
          <div class="vs">VS</div>
          <div class="team">
            <span class="team-icon">🔵🔴</span>
            Barcelona
          </div>
        </div>
        <div class="match-time">Données de démonstration</div>
      </article>

      <article class="match" data-league="Ligue 1">
        <div class="league">LIGUE 1</div>
        <div class="teams">
          <div class="team">
            <span class="team-icon">🔵</span>
            PSG
          </div>
          <div class="vs">VS</div>
          <div class="team">
            <span class="team-icon">🟠</span>
            Marseille
          </div>
        </div>
        <div class="match-time">Données de démonstration</div>
      </article>

      <article class="match" data-league="Champions League">
        <div class="league">CHAMPIONS LEAGUE</div>
        <div class="teams">
          <div class="team">
            <span class="team-icon">🔴</span>
            Liverpool
          </div>
          <div class="vs">VS</div>
          <div class="team">
            <span class="team-icon">🔵</span>
            Inter
          </div>
        </div>
        <div class="match-time">Données de démonstration</div>
      </article>

    </div>
  </section>

  <div class="ad">
    <strong>DEVENEZ PARTENAIRE</strong>
    Faites connaître votre entreprise auprès des passionnés de football.
  </div>

  <section id="resultats" style="margin-top:40px">
    <div class="section-title">
      <h2>📊 Classement</h2>
      <span>EXEMPLE</span>
    </div>

    <p style="color:var(--muted);font-size:12px;margin-bottom:12px">
      Tableau de démonstration — les données officielles seront ajoutées.
    </p>

    <div style="overflow-x:auto">
      <table class="standings">
        <thead>
          <tr>
            <th>#</th>
            <th>Équipe</th>
            <th>MJ</th>
            <th>Pts</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>1</td><td>Arsenal</td><td>0</td><td>0</td></tr>
          <tr><td>2</td><td>Liverpool</td><td>0</td><td>0</td></tr>
          <tr><td>3</td><td>Manchester City</td><td>0</td><td>0</td></tr>
          <tr><td>4</td><td>Chelsea</td><td>0</td><td>0</td></tr>
        </tbody>
      </table>
    </div>
  </section>

  <section style="margin-top:40px">
    <div class="section-title">
      <h2>📰 Actualités football</h2>
      <span>NEWS</span>
    </div>

    <div class="news-grid">
      <article class="news">
        <small>ACTUALITÉS</small>
        <h3>Le monde du football</h3>
        <p>Retrouvez bientôt les dernières actualités du football international.</p>
      </article>

      <article class="news">
        <small>COMPÉTITIONS</small>
        <h3>Les grandes compétitions</h3>
        <p>Suivez les championnats et les tournois internationaux.</p>
      </article>

      <article class="news">
        <small>HIGHLIGHTS</small>
        <h3>Les meilleurs moments</h3>
        <p>Retrouvez les résumés et vidéos publiés par les sources officielles.</p>
      </article>
    </div>
  </section>

</div>

<footer>
  <div class="logo">DTECTEUR <span>FOOT</span></div>

  <p style="margin:12px 0">
    Football. Passion. Direct.
  </p>

  <p>
    © <span id="year"></span> DTECTEUR FOOT.
    Tous droits réservés.
  </p>

  <p style="margin-top:10px">
    Plateforme indépendante. Les marques et compétitions
    appartiennent à leurs propriétaires respectifs.
  </p>
</footer>

<script>
document.getElementById("year").textContent =
  new Date().getFullYear();

const buttons = document.querySelectorAll(".filters button");
const matches = document.querySelectorAll(".match");
const search = document.getElementById("search");

let currentFilter = "all";

function filterMatches() {
  const query = search.value.toLowerCase();

  matches.forEach(match => {
    const league = match.dataset.league;
    const content = match.textContent.toLowerCase();

    const leagueOK =
      currentFilter === "all" || league === currentFilter;

    const searchOK = content.includes(query);

    match.style.display =
      leagueOK && searchOK ? "" : "none";
  });
}

buttons.forEach(button => {
  button.addEventListener("click", () => {
    buttons.forEach(b => b.classList.remove("active"));

    button.classList.add("active");
    currentFilter = button.dataset.filter;

    filterMatches();
  });
});

search.addEventListener("input", filterMatches);
</script>

</body>
</html>
