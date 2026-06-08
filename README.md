
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Institutional Transition Intelligence Framework | Executive Briefing</title>

<style>
:root{
  --navy:#06172B;
  --navy-2:#0B2747;
  --navy-3:#0E3159;
  --blue:#123E6B;
  --blue-soft:#EAF1F8;
  --gold:#C9A227;
  --gold-2:#E8CD72;
  --gray:#F5F7FA;
  --gray-2:#EEF2F6;
  --dark:#172033;
  --muted:#667085;
  --white:#FFFFFF;
  --line:#D8DEE8;
  --risk:#8A2F2F;
  --green:#2F6B4F;
  --shadow:0 18px 45px rgba(6,23,43,.14);
}

*{margin:0;padding:0;box-sizing:border-box;}

html{
  scroll-behavior:smooth;
}

body{
  font-family:Georgia,"Times New Roman",serif;
  background:var(--white);
  color:var(--dark);
  line-height:1.65;
}

#progress-bar{
  position:fixed;
  top:0;
  left:0;
  height:4px;
  width:0%;
  background:var(--gold);
  z-index:9999;
}

nav{
  position:fixed;
  top:0;
  width:100%;
  background:rgba(6,23,43,.95);
  padding:14px 7%;
  display:flex;
  justify-content:space-between;
  align-items:center;
  z-index:1000;
  backdrop-filter:blur(10px);
  border-bottom:1px solid rgba(255,255,255,.08);
}

.logo{
  color:var(--gold-2);
  font-weight:800;
  letter-spacing:.12em;
  text-transform:uppercase;
  font-size:.88rem;
}

.nav-links{
  display:flex;
  gap:18px;
  flex-wrap:wrap;
}

nav a{
  color:#E7EDF5;
  text-decoration:none;
  font-size:.88rem;
}

nav a:hover{
  color:var(--gold-2);
}

header{
  min-height:100vh;
  background:
    radial-gradient(circle at 82% 28%, rgba(201,162,39,.16), transparent 28%),
    linear-gradient(122deg, rgba(6,23,43,.99) 0%, rgba(6,23,43,.96) 48%, rgba(11,39,71,.94) 100%);
  display:flex;
  align-items:center;
  padding:120px 7% 80px;
  color:white;
  position:relative;
  overflow:hidden;
}

header:before{
  content:"";
  position:absolute;
  right:-145px;
  top:-90px;
  width:560px;
  height:125%;
  background:linear-gradient(180deg, rgba(201,162,39,.95), rgba(201,162,39,.08));
  transform:rotate(14deg);
  opacity:.72;
}

header:after{
  content:"";
  position:absolute;
  right:7%;
  bottom:10%;
  width:420px;
  height:420px;
  border:1px solid rgba(226,199,102,.22);
  border-radius:50%;
  box-shadow:0 0 0 80px rgba(255,255,255,.018), 0 0 0 160px rgba(255,255,255,.012);
}

.hero{
  max-width:1140px;
  position:relative;
  z-index:2;
}

.kicker{
  display:inline-flex;
  gap:10px;
  align-items:center;
  color:var(--gold-2);
  text-transform:uppercase;
  letter-spacing:.18em;
  font-size:.78rem;
  font-weight:bold;
  margin-bottom:24px;
  border:1px solid rgba(226,199,102,.35);
  border-radius:999px;
  padding:8px 14px;
  background:rgba(255,255,255,.04);
}

.kicker span{
  width:8px;
  height:8px;
  border-radius:50%;
  background:var(--gold-2);
  display:inline-block;
}

h1{
  font-size:clamp(3.2rem,7vw,6.8rem);
  line-height:.92;
  letter-spacing:-.055em;
  margin-bottom:28px;
  max-width:1080px;
}

.hero-subtitle{
  font-size:clamp(1.35rem,2.2vw,1.9rem);
  max-width:930px;
  color:#FFFFFF;
  margin-bottom:18px;
  font-weight:bold;
}

.hero-lede{
  font-size:clamp(1.08rem,1.8vw,1.42rem);
  max-width:930px;
  color:#DDE7F3;
  margin-bottom:16px;
}

.hero-panel{
  display:grid;
  grid-template-columns:1.15fr .85fr;
  gap:22px;
  margin-top:42px;
  max-width:1010px;
}

.panel{
  background:rgba(255,255,255,.08);
  border:1px solid rgba(255,255,255,.13);
  border-left:5px solid var(--gold);
  border-radius:14px;
  padding:24px;
  backdrop-filter:blur(8px);
}

.panel h3{
  color:white;
  font-size:1.12rem;
  margin-bottom:8px;
}

.panel p,
.panel li{
  color:#C8D5E5;
  font-size:.98rem;
}

.panel ul{
  list-style:none;
  display:grid;
  gap:7px;
}

.button-row{
  display:flex;
  gap:14px;
  flex-wrap:wrap;
  margin-top:34px;
}

.button{
  display:inline-block;
  padding:13px 24px;
  background:var(--gold);
  color:var(--navy);
  text-decoration:none;
  font-weight:bold;
  border-radius:6px;
}

.button.secondary{
  background:transparent;
  color:white;
  border:1px solid rgba(255,255,255,.28);
}

section{
  padding:88px 7%;
  scroll-margin-top:110px;
}

.section-dark{
  background:var(--navy);
  color:white;
}

.section-gray{
  background:var(--gray);
}

.section-blue{
  background:linear-gradient(135deg, var(--navy-2), var(--navy));
  color:white;
}

.section-head{
  max-width:1080px;
  margin-bottom:36px;
}

.eyebrow{
  color:var(--gold);
  text-transform:uppercase;
  letter-spacing:.18em;
  font-size:.78rem;
  font-weight:bold;
  margin-bottom:12px;
}

h2{
  font-size:clamp(2.15rem,4.5vw,4.4rem);
  line-height:1;
  letter-spacing:-.04em;
  color:var(--navy);
  margin-bottom:18px;
}

.section-dark h2,
.section-blue h2{
  color:white;
}

h3{
  margin-bottom:10px;
  color:var(--blue);
  line-height:1.2;
}

.section-dark h3,
.section-blue h3{
  color:white;
}

.intro{
  max-width:1000px;
  font-size:1.14rem;
  color:var(--muted);
}

.section-dark .intro,
.section-blue .intro{
  color:#CBD5E1;
}

.big-statement{
  font-size:clamp(1.55rem,3vw,2.75rem);
  line-height:1.22;
  margin-top:36px;
  border-left:7px solid var(--gold);
  padding:10px 0 10px 26px;
  max-width:1120px;
  color:var(--blue);
}

.section-dark .big-statement,
.section-blue .big-statement{
  color:white;
}

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(255px,1fr));
  gap:22px;
  margin-top:26px;
}

.card{
  background:white;
  padding:28px;
  border:1px solid var(--line);
  border-top:5px solid var(--gold);
  border-radius:12px;
  box-shadow:0 12px 28px rgba(6,23,43,.08);
}

.card p{
  color:var(--muted);
}

.section-dark .card,
.section-blue .card{
  background:#0E2A4A;
  border-color:rgba(226,199,102,.18);
  box-shadow:none;
}

.section-dark .card p,
.section-blue .card p{
  color:#D1D8E2;
}

.summary-metrics{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(190px,1fr));
  gap:18px;
  margin-top:30px;
}

.summary-metric{
  background:var(--navy);
  color:white;
  border-radius:14px;
  padding:24px;
  border-top:5px solid var(--gold);
  box-shadow:var(--shadow);
}

.summary-metric span{
  display:block;
  font-size:2.6rem;
  line-height:1;
  color:var(--gold-2);
  font-weight:bold;
  margin-bottom:8px;
}

.summary-metric p{
  color:#D1D8E2;
  font-weight:bold;
}

.risk-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(290px,1fr));
  gap:22px;
  margin-top:34px;
}

.risk-card{
  background:white;
  border:1px solid var(--line);
  border-left:6px solid var(--gold);
  border-radius:14px;
  padding:28px;
  box-shadow:var(--shadow);
  position:relative;
  overflow:hidden;
  transition:all .25s ease;
}

.risk-card:hover{
  transform:translateY(-4px);
  box-shadow:0 22px 48px rgba(6,23,43,.16);
}

.risk-card:before{
  content:attr(data-risk);
  position:absolute;
  right:18px;
  top:12px;
  font-size:4.8rem;
  line-height:1;
  font-weight:bold;
  color:rgba(18,62,107,.07);
  transition:all .25s ease;
}

.risk-card:hover:before{
  color:rgba(18,62,107,.14);
  transform:scale(1.08);
}

.risk-card h3{
  color:var(--navy);
  font-size:1.28rem;
  position:relative;
}

.risk-card p{
  color:var(--muted);
  position:relative;
}

.deep-risk{
  display:grid;
  grid-template-columns:.65fr 1.35fr;
  gap:28px;
  align-items:start;
}

.deep-risk-number{
  background:var(--navy);
  color:var(--gold-2);
  border-radius:18px;
  padding:34px;
  min-height:260px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  box-shadow:var(--shadow);
}

.deep-risk-number span{
  font-size:5.5rem;
  line-height:1;
  font-weight:bold;
}

.deep-risk-number p{
  color:#D1D8E2;
  font-weight:bold;
  margin-top:10px;
}

.deep-risk-content{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:18px;
}

.detail-card{
  background:white;
  border:1px solid var(--line);
  border-radius:14px;
  padding:26px;
  box-shadow:0 10px 24px rgba(6,23,43,.08);
}

.detail-card h3{
  color:var(--navy);
}

.detail-card p{
  color:var(--muted);
}

.gap-wrapper{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:24px;
  margin-top:34px;
}

.gap-box{
  background:white;
  border-radius:16px;
  padding:32px;
  border:1px solid var(--line);
  box-shadow:var(--shadow);
}

.gap-box h3{
  color:var(--navy);
  font-size:1.45rem;
  margin-bottom:18px;
}

.gap-box ul{
  list-style:none;
  display:grid;
  gap:12px;
}

.gap-box li{
  padding:12px 14px;
  background:var(--gray);
  border-radius:8px;
  color:var(--dark);
  font-weight:bold;
}

.check li:before{
  content:"✓ ";
  color:var(--green);
  font-weight:bold;
}

.miss li:before{
  content:"✕ ";
  color:var(--risk);
  font-weight:bold;
}

.lifecycle{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
  margin-top:34px;
}

.life-step{
  background:white;
  color:var(--dark);
  border-radius:16px;
  padding:30px;
  border:1px solid rgba(255,255,255,.2);
  box-shadow:0 16px 34px rgba(0,0,0,.16);
  position:relative;
}

.life-step:after{
  content:"";
  position:absolute;
  right:-17px;
  top:50%;
  transform:translateY(-50%);
  width:18px;
  height:2px;
  background:var(--gold);
}

.life-step:last-child:after{
  display:none;
}

.life-step span{
  display:inline-block;
  background:rgba(201,162,39,.14);
  color:var(--gold);
  border:1px solid rgba(201,162,39,.35);
  border-radius:999px;
  padding:6px 12px;
  font-weight:bold;
  font-family:"Courier New",monospace;
  margin-bottom:16px;
}

.life-step h3{
  color:var(--navy);
  font-size:1.42rem;
}

.life-step ul{
  margin-top:14px;
  padding-left:18px;
  color:var(--muted);
}

.life-step li{
  margin-bottom:7px;
}

.pilot-grid{
  display:grid;
  grid-template-columns:.9fr 1.1fr;
  gap:24px;
  align-items:stretch;
  margin-top:34px;
}

.pilot-card{
  background:white;
  border-radius:16px;
  padding:32px;
  border:1px solid var(--line);
  box-shadow:var(--shadow);
}

.pilot-card h3{
  color:var(--navy);
  font-size:1.42rem;
}

.pilot-card p,
.pilot-card li{
  color:var(--muted);
}

.pilot-card ul{
  list-style:none;
  display:grid;
  gap:12px;
  margin-top:18px;
}

.pilot-card li{
  padding:12px 14px;
  background:var(--gray);
  border-radius:8px;
  font-weight:bold;
}

.pilot-card li:before{
  content:"• ";
  color:var(--gold);
}

.future{
  background:
    radial-gradient(circle at 12% 18%, rgba(201,162,39,.12), transparent 24%),
    linear-gradient(135deg, var(--navy), var(--navy-3));
  border-radius:22px;
  padding:46px;
  margin-top:34px;
  color:white;
  box-shadow:0 22px 48px rgba(6,23,43,.22);
}

.future h3{
  color:var(--gold-2);
  font-size:clamp(1.7rem,3vw,3rem);
  line-height:1.1;
}

.future .quote{
  font-size:clamp(1.4rem,2.5vw,2.4rem);
  margin:24px 0;
  line-height:1.18;
}

.future-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:24px;
  margin-top:28px;
}

.future-box{
  background:rgba(255,255,255,.08);
  border:1px solid rgba(255,255,255,.12);
  border-radius:14px;
  padding:24px;
}

.future-box h4{
  color:white;
  font-size:1.2rem;
  margin-bottom:12px;
}

.future-box ul{
  list-style:none;
  display:grid;
  gap:10px;
  color:#D1D8E2;
}

.future-box li:before{
  content:"— ";
  color:var(--gold-2);
}

.outcomes{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
  gap:22px;
  margin-top:28px;
}

.outcome{
  padding:30px;
  background:white;
  border:1px solid var(--line);
  border-top:6px solid var(--gold);
  border-radius:12px;
  box-shadow:0 8px 22px rgba(6,23,43,.08);
}

.outcome span{
  display:block;
  font-size:1.7rem;
  line-height:1.08;
  font-weight:bold;
  color:var(--blue);
  margin-bottom:12px;
}

.outcome p{
  color:var(--muted);
}

.closing{
  text-align:center;
  max-width:1000px;
  margin:0 auto;
}

.closing h2{
  font-size:clamp(2.4rem,5vw,5rem);
}

.closing p{
  font-size:1.25rem;
  color:var(--muted);
  margin-top:18px;
}

.closing .final-line{
  margin-top:32px;
  font-size:clamp(1.5rem,3vw,2.5rem);
  color:var(--blue);
  font-weight:bold;
  line-height:1.2;
}

footer{
  background:#030D19;
  color:#CBD5E1;
  padding:38px 7%;
  border-top:1px solid rgba(255,255,255,.08);
}

.footer-grid{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:24px;
  align-items:center;
}

footer strong{
  color:white;
}

@media(max-width:1050px){
  .lifecycle{
    grid-template-columns:1fr 1fr;
  }

  .life-step:after{
    display:none;
  }

  .deep-risk{
    grid-template-columns:1fr;
  }
}

@media(max-width:900px){
  .hero-panel,
  .gap-wrapper,
  .pilot-grid,
  .future-grid,
  .footer-grid,
  .deep-risk-content{
    grid-template-columns:1fr;
  }

  header:before,
  header:after{
    display:none;
  }
}

@media(max-width:768px){
  nav{
    align-items:flex-start;
    flex-direction:column;
    gap:10px;
  }

  .nav-links{
    gap:12px;
  }

  nav a{
    font-size:.84rem;
  }

  header{
    padding-top:165px;
  }

  section{
    padding:72px 7%;
    scroll-margin-top:150px;
  }

  .lifecycle{
    grid-template-columns:1fr;
  }
}
</style>
</head>

<body>

<div id="progress-bar" aria-hidden="true"></div>

<nav>
  <div class="logo">ITIF Executive Briefing</div>
  <div class="nav-links">
    <a href="#summary">Summary</a>
    <a href="#why">Why</a>
    <a href="#risks">Risks</a>
    <a href="#gap">Gap</a>
    <a href="#framework">Framework</a>
    <a href="#pilot">Pilot</a>
    <a href="#future">Decision Advantage</a>
  </div>
</nav>

<header>
  <div class="hero">
    <div class="kicker"><span></span>Massachusetts Department of Correction</div>

    <h1>Institutional Transition Intelligence Framework</h1>

    <p class="hero-subtitle">
      Preserving Organizational Capability During Workforce Transition
    </p>

    <p class="hero-lede">
      The Department preserves records exceptionally well. The next challenge is preserving operational intelligence.
    </p>

    <div class="hero-panel">
      <div class="panel">
        <h3>Executive Thesis</h3>
        <p>
          Every transition creates risk. Retirements, promotions, transfers, resignations, and leadership changes can remove context, judgment, relationships, and hard-earned operational lessons from the agency.
        </p>
      </div>

      <div class="panel">
        <h3>Core Message</h3>
        <ul>
          <li>The risk is not simply vacancies.</li>
          <li>The risk is capability loss.</li>
          <li>ITIF preserves capability before it becomes organizational loss.</li>
        </ul>
      </div>
    </div>

    <div class="button-row">
      <a href="#summary" class="button">View Briefing ↓</a>
      <a href="#pilot" class="button secondary">Pilot Proposal</a>
    </div>
  </div>
</header>

<section id="summary" class="section-gray">
  <div class="section-head">
    <div class="eyebrow">Executive Summary</div>
    <h2>A continuity framework designed to reduce organizational risk.</h2>
    <p class="intro">
      ITIF is a structured process for identifying, capturing, organizing, preserving, and applying operational intelligence during periods of workforce transition and organizational change.
    </p>
  </div>

  <div class="summary-metrics">
    <div class="summary-metric">
      <span>7</span>
      <p>Organizational Risks</p>
    </div>

    <div class="summary-metric">
      <span>1</span>
      <p>Continuity Framework</p>
    </div>

    <div class="summary-metric">
      <span>1</span>
      <p>Program Owner</p>
    </div>

    <div class="summary-metric">
      <span>0</span>
      <p>New Enterprise Platforms</p>
    </div>
  </div>

  <div class="big-statement">
    The purpose of ITIF is not to preserve documents. The purpose of ITIF is to preserve organizational capability.
  </div>
</section>

<section id="why">
  <div class="section-head">
    <div class="eyebrow">Why This Matters</div>
    <h2>Workforce transitions create more than staffing gaps.</h2>
    <p class="intro">
      When experienced employees retire, transfer, promote, or leave service, the Department may lose more than a person. It may lose historical context, decision logic, operational judgment, stakeholder relationships, lessons learned, and informal workflows that are not fully preserved in formal documentation.
    </p>
  </div>

  <div class="grid">
    <div class="card">
      <h3>Records Are Not Enough</h3>
      <p>Policies, procedures, reports, and personnel files preserve official information. They do not always preserve why decisions were made or how work actually gets done.</p>
    </div>

    <div class="card">
      <h3>Capability Can Leave Quietly</h3>
      <p>Two people can hold the same title, but only one may know the historical pitfalls, stakeholder dynamics, and process logic behind the role.</p>
    </div>

    <div class="card">
      <h3>Continuity Must Be Designed</h3>
      <p>Institutional memory cannot rely only on individual employees. It must be captured, organized, preserved, and applied through a repeatable process.</p>
    </div>
  </div>

  <div class="big-statement">
    The challenge is not documentation. The challenge is preserving operational capability through transition.
  </div>
</section>

<section id="risks" class="section-gray">
  <div class="section-head">
    <div class="eyebrow">Organizational Risk Exposure</div>
    <h2>Seven risks make institutional intelligence urgent.</h2>
    <p class="intro">
      These risks are not separate problems. They are connected continuity risks that increase when institutional knowledge is not captured before it leaves, fragments, or becomes inaccessible.
    </p>
  </div>

  <div class="risk-grid">
    <div class="risk-card" data-risk="01">
      <h3>Retirement Eligibility & Knowledge Loss</h3>
      <p>The risk is not simply vacancies; it is the loss of context, judgment, stakeholder knowledge, and institutional memory.</p>
    </div>

    <div class="risk-card" data-risk="02">
      <h3>High Turnover Facilities</h3>
      <p>Facilities with persistent turnover can repeatedly relearn the same lessons without inherited knowledge.</p>
    </div>

    <div class="risk-card" data-risk="03">
      <h3>Policy Resistance & Change Adoption</h3>
      <p>Resistance is often treated as a people problem when it may actually be an intelligence problem.</p>
    </div>

    <div class="risk-card" data-risk="04">
      <h3>Repeated Organizational Mistakes</h3>
      <p>Projects fail, lessons are learned, people change, and years later the same mistakes recur.</p>
    </div>

    <div class="risk-card" data-risk="05">
      <h3>Succession Planning Gaps</h3>
      <p>Succession planning should ask what knowledge must transfer, not only who may replace whom.</p>
    </div>

    <div class="risk-card" data-risk="06">
      <h3>Executive Decision Blind Spots</h3>
      <p>Leaders need historical context, lessons learned, prior recommendations, and operational insight.</p>
    </div>

    <div class="risk-card" data-risk="07">
      <h3>Informal Expert Dependency</h3>
      <p>Critical operational capability can become concentrated in individual knowledge holders.</p>
    </div>
  </div>
</section>

<section id="risk1">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>01</span>
      <p>Retirement Eligibility & Knowledge Loss</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>A significant number of employees may possess decades of institutional knowledge and retirement eligibility.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>The risk is not only vacancies. The deeper risk is capability loss when historical context and judgment leave with the employee.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Capture role-based intelligence, decision logic, stakeholder knowledge, pitfalls, and lessons learned before departure.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>Future employees inherit more than the title. They inherit the intelligence required to perform effectively.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk2" class="section-gray">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>02</span>
      <p>High Turnover Facilities</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Some facilities or operational areas experience persistent turnover, leadership changes, and staffing instability.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>The institution repeatedly starts over, relearning lessons that previous teams already discovered.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Preserve known risks, best practices, prior recommendations, and lessons learned from previous leadership and teams.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>The institution becomes smarter than the individual and maintains continuity despite staff movement.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk3">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>03</span>
      <p>Policy Resistance & Change Adoption</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Policy, technology, and procedural changes often encounter resistance during implementation.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>The organization may know that a policy failed but lose the reasons why adoption failed.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Capture resistance points, adoption barriers, communication gaps, operational impacts, and implementation feedback.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>Future change efforts are informed by prior implementation intelligence instead of repeated trial and error.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk4" class="section-gray">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>04</span>
      <p>Repeated Organizational Mistakes</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Projects and initiatives generate valuable lessons, but those lessons often disappear when personnel change.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>The same project can fail years later for reasons already known by the organization but no longer accessible.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Formalize lessons learned, project closeouts, after-action reviews, and implementation histories.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>Experience becomes reusable institutional intelligence instead of temporary individual memory.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk5">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>05</span>
      <p>Succession Planning Gaps</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Succession planning often identifies who might replace someone without identifying what knowledge must transfer.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>A successor may inherit the position but not the context, relationships, pitfalls, or operating logic required to succeed.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Capture role-based intelligence, critical relationships, decision patterns, recurring challenges, and transition notes.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>Succession becomes a transfer of capability, not only a transfer of responsibility.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk6" class="section-gray">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>06</span>
      <p>Executive Decision Blind Spots</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Leaders frequently require historical context, prior recommendations, and operational insight when making decisions.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>Critical context may be scattered across emails, spreadsheets, documents, meetings, and individual memories.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Make institutional intelligence searchable, organized, and available before decisions become urgent.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>Executives gain decision advantage through better access to what the Department already knows.</p>
      </div>
    </div>
  </div>
</section>

<section id="risk7">
  <div class="deep-risk">
    <div class="deep-risk-number">
      <span>07</span>
      <p>Informal Expert Dependency</p>
    </div>
    <div class="deep-risk-content">
      <div class="detail-card">
        <h3>Problem</h3>
        <p>Organizations often depend on a small number of experienced individuals who hold unique institutional knowledge.</p>
      </div>
      <div class="detail-card">
        <h3>Risk</h3>
        <p>When those individuals leave, retire, transfer, or promote, critical operational capability can leave with them.</p>
      </div>
      <div class="detail-card">
        <h3>ITIF Response</h3>
        <p>Identify informal experts and preserve their knowledge through structured interviews, mapping, and classified entries.</p>
      </div>
      <div class="detail-card">
        <h3>Expected Outcome</h3>
        <p>The Department reduces overreliance on individual memory and strengthens institutional resilience.</p>
      </div>
    </div>
  </div>
</section>

<section id="gap" class="section-gray">
  <div class="section-head">
    <div class="eyebrow">The Continuity Gap</div>
    <h2>The Department may retain the record but lose the reasoning.</h2>
    <p class="intro">
      ITIF does not replace existing documentation systems. It fills the gap between formal records and operational intelligence.
    </p>
  </div>

  <div class="gap-wrapper">
    <div class="gap-box check">
      <h3>Current Systems Preserve</h3>
      <ul>
        <li>Policies</li>
        <li>Procedures</li>
        <li>Personnel Records</li>
        <li>Reports</li>
        <li>Compliance Documentation</li>
      </ul>
    </div>

    <div class="gap-box miss">
      <h3>Current Systems Often Miss</h3>
      <ul>
        <li>Operational Judgment</li>
        <li>Historical Context</li>
        <li>Lessons Learned</li>
        <li>Decision Logic</li>
        <li>Stakeholder Relationships</li>
        <li>Informal Workflows</li>
      </ul>
    </div>
  </div>

  <div class="big-statement">
    ITIF is not about storing more documents. It is about preserving the intelligence that explains how the institution actually works.
  </div>
</section>

<section id="framework" class="section-blue">
  <div class="section-head">
    <div class="eyebrow">Introducing ITIF</div>
    <h2>A repeatable process for institutional continuity.</h2>
    <p class="intro">
      The Institutional Transition Intelligence Framework establishes a structured process for identifying, capturing, organizing, preserving, and applying institutional intelligence before it is lost.
    </p>
  </div>

  <div class="lifecycle">
    <div class="life-step">
      <span>01</span>
      <h3>Capture</h3>
      <p>Collect intelligence before, during, and after workforce transitions.</p>
      <ul>
        <li>Retirement interviews</li>
        <li>Transition interviews</li>
        <li>Workflow mapping</li>
        <li>Lessons learned reviews</li>
        <li>Operational debriefs</li>
      </ul>
    </div>

    <div class="life-step">
      <span>02</span>
      <h3>Organize</h3>
      <p>Convert experience into searchable and usable institutional intelligence.</p>
      <ul>
        <li>Metadata</li>
        <li>Classification</li>
        <li>Taxonomy</li>
        <li>Governance</li>
        <li>Validation</li>
      </ul>
    </div>

    <div class="life-step">
      <span>03</span>
      <h3>Preserve</h3>
      <p>Store institutional intelligence in a structured repository that can be retrieved and reused.</p>
      <ul>
        <li>Knowledge repository</li>
        <li>Source attribution</li>
        <li>Access controls</li>
        <li>Retention standards</li>
        <li>Searchable entries</li>
      </ul>
    </div>

    <div class="life-step">
      <span>04</span>
      <h3>Apply</h3>
      <p>Use intelligence to strengthen continuity, planning, and decision-making.</p>
      <ul>
        <li>Onboarding</li>
        <li>Succession planning</li>
        <li>Leadership development</li>
        <li>Policy implementation</li>
        <li>Operational planning</li>
      </ul>
    </div>
  </div>

  <div class="big-statement">
    The archive is not the strategy. The strategy is a continuity framework that turns experience into institutional capability.
  </div>
</section>

<section id="ownership">
  <div class="section-head">
    <div class="eyebrow">Governance & Ownership</div>
    <h2>One program owner can manage the first version.</h2>
    <p class="intro">
      The framework requires clear ownership, intake standards, review procedures, and reporting discipline. It does not require a new unit to begin.
    </p>
  </div>

  <div class="grid">
    <div class="card">
      <h3>Program Ownership</h3>
      <p>Coordinate intake, maintain standards, manage the pilot scope, and ensure captured intelligence remains usable.</p>
    </div>

    <div class="card">
      <h3>Quality Review</h3>
      <p>Validate entries for relevance, completeness, sensitivity, and operational value before they are preserved.</p>
    </div>

    <div class="card">
      <h3>Governance Standards</h3>
      <p>Maintain metadata rules, taxonomy, permissions, retention standards, and escalation pathways.</p>
    </div>

    <div class="card">
      <h3>Reporting</h3>
      <p>Track intake activity, usage, recurring themes, continuity risks, and areas where leadership may need better intelligence.</p>
    </div>
  </div>
</section>

<section id="pilot" class="section-gray">
  <div class="section-head">
    <div class="eyebrow">Pilot Proposal</div>
    <h2>Start with a controlled pilot.</h2>
    <p class="intro">
      The initial version should begin as a controlled pilot managed by one program owner using existing Department tools. The goal is to prove operational value, establish intake standards, and demonstrate how institutional intelligence can support continuity before expanding the model.
    </p>
  </div>

  <div class="pilot-grid">
    <div class="pilot-card">
      <h3>Initial Operating Model</h3>
      <ul>
        <li>One Program Owner</li>
        <li>Controlled pilot scope</li>
        <li>Existing Microsoft infrastructure</li>
        <li>Defined intake process</li>
        <li>Clear governance standards</li>
      </ul>
    </div>

    <div class="pilot-card">
      <h3>Suggested Pilot Focus</h3>
      <p>
        Begin where continuity risk is already visible: retirement-eligible roles, high-turnover facilities, leadership transitions, major policy implementation, or a known operational process that depends heavily on informal knowledge.
      </p>
      <ul>
        <li>SharePoint for repository structure</li>
        <li>Microsoft Forms for intake</li>
        <li>Microsoft Lists for classification</li>
        <li>Power BI for visibility</li>
      </ul>
    </div>
  </div>
</section>

<section id="future">
  <div class="section-head">
    <div class="eyebrow">Decision Advantage</div>
    <h2>Institutional intelligence should be accessible before decisions become urgent.</h2>
    <p class="intro">
      The long-term value of ITIF is not simply preservation. It is the ability to retrieve institutional knowledge when leaders, managers, and teams need it.
    </p>
  </div>

  <div class="future">
    <h3>Executive Decision Support</h3>
    <div class="quote">Imagine a Deputy Commissioner asks: “What do we know about onboarding?”</div>

    <div class="future-grid">
      <div class="future-box">
        <h4>Without ITIF</h4>
        <ul>
          <li>Five meetings</li>
          <li>Three emails</li>
          <li>Four spreadsheets</li>
          <li>Two phone calls</li>
          <li>Fragmented memory</li>
        </ul>
      </div>

      <div class="future-box">
        <h4>With ITIF</h4>
        <ul>
          <li>Prior lessons learned</li>
          <li>Known risks</li>
          <li>Implementation barriers</li>
          <li>Previous recommendations</li>
          <li>Usable institutional intelligence</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section class="section-gray">
  <div class="section-head">
    <div class="eyebrow">Strategic Outcomes</div>
    <h2>What ITIF strengthens over time.</h2>
    <p class="intro">
      The framework creates value by converting transition risk into continuity capability.
    </p>
  </div>

  <div class="outcomes">
    <div class="outcome">
      <span>Operational Continuity</span>
      <p>Preserves lessons, workflows, and role-based intelligence across personnel changes.</p>
    </div>

    <div class="outcome">
      <span>Organizational Learning</span>
      <p>Reduces repeated mistakes by making lessons learned retrievable and reusable.</p>
    </div>

    <div class="outcome">
      <span>Succession Readiness</span>
      <p>Improves transition planning by identifying what knowledge must transfer, not only who may replace whom.</p>
    </div>

    <div class="outcome">
      <span>Decision Support</span>
      <p>Gives leaders better access to historical context, operational insight, and implementation intelligence.</p>
    </div>

    <div class="outcome">
      <span>Workforce Resilience</span>
      <p>Supports continuity when turnover, retirement, promotion, or transfer creates instability.</p>
    </div>

    <div class="outcome">
      <span>Change Adoption</span>
      <p>Improves future implementation by preserving resistance points, barriers, and lessons learned.</p>
    </div>
  </div>
</section>

<section id="possibilities">
  <div class="section-head">
    <div class="eyebrow">Future Possibilities</div>
    <h2>Toward searchable institutional intelligence.</h2>
    <p class="intro">
      Over time, ITIF could support a searchable institutional intelligence capability where leaders can retrieve prior lessons, risk patterns, implementation history, and operational context by topic.
    </p>
  </div>

  <div class="grid">
    <div class="card">
      <h3>Search: Onboarding</h3>
      <p>Retrieve onboarding lessons, preparation gaps, candidate transition issues, and prior recommendations.</p>
    </div>

    <div class="card">
      <h3>Search: Facility Turnover</h3>
      <p>Identify recurring turnover patterns, facility-specific risks, prior interventions, and lessons learned.</p>
    </div>

    <div class="card">
      <h3>Search: Policy Implementation</h3>
      <p>Review adoption barriers, communication gaps, operational impacts, and implementation feedback.</p>
    </div>

    <div class="card">
      <h3>Search: Leadership Transition</h3>
      <p>Access role-based knowledge, stakeholder maps, historical issues, and transition guidance.</p>
    </div>
  </div>
</section>

<section>
  <div class="closing">
    <div class="eyebrow">Closing Statement</div>
    <h2>The purpose of ITIF is not to preserve documents.</h2>
    <p>
      The purpose of ITIF is to preserve organizational capability during workforce transition and organizational change.
    </p>
    <div class="final-line">
      Preserve capability before it becomes organizational loss.
    </div>
  </div>
</section>

<footer>
  <div class="footer-grid">
    <div>
      <strong>Institutional Transition Intelligence Framework</strong><br/>
      Risk Exposure | Continuity Gap | Framework | Pilot | Decision Advantage
    </div>
    <div>
      Massachusetts Department of Correction<br/>
      Workforce Development Division | June 2026
    </div>
  </div>
</footer>

<script>
(function(){
  const progressBar = document.getElementById("progress-bar");

  if(!progressBar){
    return;
  }

  function updateProgress(){
    const scrollTop = window.pageYOffset || document.documentElement.scrollTop;
    const scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
    const progress = scrollHeight > 0 ? (scrollTop / scrollHeight) * 100 : 0;
    progressBar.style.width = progress + "%";
  }

  window.addEventListener("scroll", updateProgress, { passive:true });
  window.addEventListener("resize", updateProgress);
  updateProgress();
})();
</script>

</body>
</html>

