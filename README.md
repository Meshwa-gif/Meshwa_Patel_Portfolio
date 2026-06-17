<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Meshwa Patel — Data Analyst Portfolio</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --navy:#0C1A2E;
  --navy-mid:#0F2440;
  --navy-light:#1A3A5C;
  --blue:#185FA5;
  --blue-light:#E6F1FB;
  --blue-mid:#B5D4F4;
  --blue-accent:#378ADD;
  --text-on-navy:#E6F1FB;
  --text-muted-navy:#6B9DC9;
  --white:#FFFFFF;
  --gray-bg:#F4F7FB;
  --gray-border:#D0DCF0;
  --text-dark:#0C1A2E;
  --text-mid:#2C4A6E;
  --text-muted:#5A7A9A;
}
html{scroll-behavior:smooth}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;color:var(--text-dark);background:var(--white);line-height:1.6}

/* NAV */
nav{position:sticky;top:0;z-index:100;background:var(--navy);border-bottom:1px solid var(--navy-light);padding:0 2rem}
.nav-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;height:56px}
.nav-logo{font-size:15px;font-weight:600;color:var(--text-on-navy);letter-spacing:.02em}
.nav-logo span{color:var(--blue-accent)}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{font-size:13px;color:var(--text-muted-navy);text-decoration:none;transition:color .2s}
.nav-links a:hover{color:var(--text-on-navy)}
.nav-badge{font-size:11px;background:var(--blue);color:var(--white);padding:3px 10px;border-radius:20px}

/* HERO */
.hero{background:var(--navy);padding:5rem 2rem 4rem;text-align:center}
.hero-inner{max-width:800px;margin:0 auto}
.hero-eyebrow{font-size:12px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;color:var(--blue-accent);margin-bottom:1.25rem}
.hero h1{font-size:clamp(2.2rem,5vw,3.5rem);font-weight:600;color:var(--white);line-height:1.15;margin-bottom:1rem}
.hero h1 span{color:var(--blue-accent)}
.hero-sub{font-size:1.05rem;color:var(--text-muted-navy);max-width:600px;margin:0 auto 2rem}
.hero-tools{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-bottom:2.5rem}
.tool-pill{font-size:12px;padding:4px 14px;border:1px solid var(--navy-light);border-radius:20px;color:var(--text-muted-navy);background:rgba(255,255,255,.04)}
.hero-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem;max-width:700px;margin:0 auto 2.5rem}
.stat-card{background:rgba(255,255,255,.06);border:1px solid var(--navy-light);border-radius:12px;padding:1.25rem 1rem;text-align:center}
.stat-num{font-size:1.6rem;font-weight:600;color:var(--white);display:block}
.stat-label{font-size:11px;color:var(--text-muted-navy);margin-top:2px;display:block}
.hero-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
.btn-primary{padding:10px 24px;background:var(--blue-accent);color:var(--white);border:none;border-radius:8px;font-size:14px;font-weight:500;cursor:pointer;text-decoration:none;transition:background .2s}
.btn-primary:hover{background:#185FA5}
.btn-outline{padding:10px 24px;background:transparent;color:var(--text-on-navy);border:1px solid var(--navy-light);border-radius:8px;font-size:14px;font-weight:500;cursor:pointer;text-decoration:none;transition:all .2s}
.btn-outline:hover{border-color:var(--blue-accent);color:var(--blue-accent)}

/* SECTIONS */
section{padding:5rem 2rem}
.section-inner{max-width:1100px;margin:0 auto}
.section-label{font-size:11px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;color:var(--blue);margin-bottom:.5rem}
.section-title{font-size:clamp(1.6rem,3vw,2.2rem);font-weight:600;color:var(--text-dark);margin-bottom:.5rem}
.section-sub{font-size:15px;color:var(--text-muted);margin-bottom:3rem}

/* SKILLS */
.skills-section{background:var(--gray-bg)}
.skills-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1rem}
.skill-card{background:var(--white);border:1px solid var(--gray-border);border-radius:12px;padding:1.5rem}
.skill-icon{width:40px;height:40px;background:var(--blue-light);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;margin-bottom:1rem}
.skill-name{font-size:14px;font-weight:600;color:var(--text-dark);margin-bottom:.25rem}
.skill-desc{font-size:12px;color:var(--text-muted);margin-bottom:.75rem}
.skill-tags{display:flex;flex-wrap:wrap;gap:5px}
.skill-tag{font-size:11px;padding:2px 8px;background:var(--blue-light);color:var(--blue);border-radius:6px;font-weight:500}

/* PROJECTS */
.projects-section{background:var(--white)}
.projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:1.5rem}
.proj-card{border:1px solid var(--gray-border);border-radius:14px;overflow:hidden;transition:box-shadow .2s,transform .2s;background:var(--white)}
.proj-card:hover{box-shadow:0 8px 30px rgba(12,26,46,.1);transform:translateY(-2px)}
.proj-top{background:var(--navy);padding:1.25rem 1.5rem}
.proj-num{font-size:11px;font-weight:500;color:var(--text-muted-navy);letter-spacing:.08em;text-transform:uppercase;margin-bottom:.5rem}
.proj-title{font-size:16px;font-weight:600;color:var(--white);margin-bottom:.25rem}
.proj-type{font-size:12px;color:var(--blue-accent)}
.proj-body{padding:1.25rem 1.5rem}
.proj-desc{font-size:13px;color:var(--text-mid);line-height:1.6;margin-bottom:1rem}
.proj-metrics{display:grid;grid-template-columns:repeat(3,1fr);gap:.5rem;margin-bottom:1rem}
.proj-metric{background:var(--blue-light);border-radius:8px;padding:.6rem .5rem;text-align:center}
.proj-metric-num{font-size:13px;font-weight:600;color:var(--blue);display:block}
.proj-metric-label{font-size:10px;color:var(--text-muted);display:block;margin-top:1px}
.proj-tags{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:1rem}
.proj-tag{font-size:11px;padding:2px 8px;background:var(--gray-bg);color:var(--text-mid);border-radius:6px}
.proj-footer{border-top:1px solid var(--gray-border);padding-top:1rem;display:flex;gap:8px}
.proj-link{flex:1;text-align:center;padding:8px;border-radius:8px;font-size:12px;font-weight:500;text-decoration:none;transition:all .2s}
.proj-link-primary{background:var(--navy);color:var(--white)}
.proj-link-primary:hover{background:var(--blue)}
.proj-link-secondary{background:var(--blue-light);color:var(--blue)}
.proj-link-secondary:hover{background:var(--blue-mid)}

/* EXPERIENCE */
.exp-section{background:var(--gray-bg)}
.exp-list{display:flex;flex-direction:column;gap:1rem}
.exp-card{background:var(--white);border:1px solid var(--gray-border);border-radius:12px;padding:1.5rem;display:flex;gap:1.5rem}
.exp-left{flex-shrink:0;width:110px}
.exp-dates{font-size:11px;color:var(--text-muted);line-height:1.5}
.exp-dot{width:10px;height:10px;border-radius:50%;background:var(--blue-accent);margin:0 auto 8px}
.exp-title{font-size:15px;font-weight:600;color:var(--text-dark);margin-bottom:.25rem}
.exp-company{font-size:13px;color:var(--blue);margin-bottom:.75rem}
.exp-bullets{list-style:none;padding:0}
.exp-bullets li{font-size:13px;color:var(--text-mid);padding:.25rem 0 .25rem 1rem;position:relative;line-height:1.5}
.exp-bullets li::before{content:"→";position:absolute;left:0;color:var(--blue-accent);font-size:12px}

/* CERTS */
.certs-section{background:var(--navy)}
.certs-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1rem}
.cert-card{background:rgba(255,255,255,.06);border:1px solid var(--navy-light);border-radius:12px;padding:1.25rem}
.cert-icon{font-size:24px;margin-bottom:.75rem}
.cert-name{font-size:13px;font-weight:500;color:var(--text-on-navy);margin-bottom:.25rem}
.cert-issuer{font-size:11px;color:var(--text-muted-navy)}

/* CONTACT */
.contact-section{background:var(--white);text-align:center}
.contact-inner{max-width:600px;margin:0 auto}
.contact-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-top:2rem}

/* FOOTER */
footer{background:var(--navy);padding:1.5rem 2rem;text-align:center}
footer p{font-size:12px;color:var(--text-muted-navy)}

@media(max-width:600px){
  .hero-stats{grid-template-columns:repeat(2,1fr)}
  .exp-card{flex-direction:column;gap:.75rem}
  .exp-left{width:auto;display:flex;align-items:center;gap:.75rem}
  .exp-dot{margin:0}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <span class="nav-logo"><span>M</span>eshwa.dev</span>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <span class="nav-badge">👋 Open to Work</span>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="about">
  <div class="hero-inner">
    <div class="hero-eyebrow">Data Analyst · Charleston, WV</div>
    <h1>Meshwa <span>Patel</span></h1>
    <p class="hero-sub">Turning messy datasets into decisions — Power BI dashboards, Python ML models, and SQL pipelines that cut costs, reduce risk, and move business forward.</p>
    <div class="hero-tools">
      <span class="tool-pill">Power BI</span>
      <span class="tool-pill">Python</span>
      <span class="tool-pill">SQL</span>
      <span class="tool-pill">Tableau</span>
      <span class="tool-pill">ETL Pipelines</span>
      <span class="tool-pill">Machine Learning</span>
      <span class="tool-pill">scikit-learn</span>
      <span class="tool-pill">DAX</span>
      <span class="tool-pill">R</span>
      <span class="tool-pill">NLP</span>
    </div>
    <div class="hero-stats">
      <div class="stat-card"><span class="stat-num">3+</span><span class="stat-label">Years Experience</span></div>
      <div class="stat-card"><span class="stat-num">5</span><span class="stat-label">Portfolio Projects</span></div>
      <div class="stat-card"><span class="stat-num">135%</span><span class="stat-label">AAPL Return Found</span></div>
      <div class="stat-card"><span class="stat-num">0.834</span><span class="stat-label">Best Model AUC</span></div>
    </div>
    <div class="hero-btns">
      <a href="#projects" class="btn-primary">View my work →</a>
      <a href="mailto:meshwapatel2508@gmail.com" class="btn-outline">✉ Get in touch</a>
      <a href="https://www.linkedin.com/in/meshwapatel-2b24a8385" target="_blank" class="btn-outline">LinkedIn ↗</a>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section class="skills-section" id="skills">
  <div class="section-inner">
    <div class="section-label">What I work with</div>
    <h2 class="section-title">Skills & Tools</h2>
    <p class="section-sub">End-to-end analytics across the full data stack</p>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-icon">📊</div>
        <div class="skill-name">Business Intelligence</div>
        <div class="skill-desc">Building dashboards that drive decisions</div>
        <div class="skill-tags"><span class="skill-tag">Power BI</span><span class="skill-tag">Tableau</span><span class="skill-tag">DAX</span><span class="skill-tag">ETL</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🐍</div>
        <div class="skill-name">Python & ML</div>
        <div class="skill-desc">End-to-end analytics and predictive modeling</div>
        <div class="skill-tags"><span class="skill-tag">Python</span><span class="skill-tag">scikit-learn</span><span class="skill-tag">pandas</span><span class="skill-tag">seaborn</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🗄️</div>
        <div class="skill-name">SQL & Data Engineering</div>
        <div class="skill-desc">Complex queries, JOINs, and data pipelines</div>
        <div class="skill-tags"><span class="skill-tag">SQL</span><span class="skill-tag">SQLite</span><span class="skill-tag">ERP Systems</span><span class="skill-tag">R</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🧠</div>
        <div class="skill-name">NLP & Advanced Analytics</div>
        <div class="skill-desc">Text analysis and classification at scale</div>
        <div class="skill-tags"><span class="skill-tag">TF-IDF</span><span class="skill-tag">NLP</span><span class="skill-tag">Classification</span><span class="skill-tag">ROC-AUC</span></div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section class="projects-section" id="projects">
  <div class="section-inner">
    <div class="section-label">Portfolio</div>
    <h2 class="section-title">5 projects. Real data. Real results.</h2>
    <p class="section-sub">Every project built from scratch with production-quality code and business recommendations</p>
    <div class="projects-grid">

      <!-- PROJECT 1 -->
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-num">Project 01</div>
          <div class="proj-title">Superstore Sales Dashboard</div>
          <div class="proj-type">Power BI · Business Intelligence</div>
        </div>
        <div class="proj-body">
          <p class="proj-desc">Interactive Power BI dashboard analyzing 9,994 US retail transactions across 4 regions and 17 sub-categories. DAX measures for dynamic KPI cards with slicer-driven cross-filtering.</p>
          <div class="proj-metrics">
            <div class="proj-metric"><span class="proj-metric-num">$2.3M</span><span class="proj-metric-label">Total Sales</span></div>
            <div class="proj-metric"><span class="proj-metric-num">12.47%</span><span class="proj-metric-label">Profit Margin</span></div>
            <div class="proj-metric"><span class="proj-metric-num">6</span><span class="proj-metric-label">Visuals Built</span></div>
          </div>
          <div class="proj-tags"><span class="proj-tag">Power BI</span><span class="proj-tag">DAX</span><span class="proj-tag">Excel</span><span class="proj-tag">KPI Design</span></div>
          <div class="proj-footer">
            <a href="https://github.com/Meshwa-gif/Superstore-PowerBI-Dashboard" target="_blank" class="proj-link proj-link-primary" style="flex:1">View on GitHub →</a>
            
          </div>
        </div>
      </div>

      <!-- PROJECT 2 -->
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-num">Project 02</div>
          <div class="proj-title">AAPL Stock Market Analysis</div>
          <div class="proj-type">Python · Financial Analytics</div>
        </div>
        <div class="proj-body">
          <p class="proj-desc">5-year analysis of Apple stock data — moving averages, daily returns, volatility clustering, volume patterns, and cross-stock correlation with AMZN, GOOGL, MSFT, and TSLA.</p>
          <div class="proj-metrics">
            <div class="proj-metric"><span class="proj-metric-num">135%</span><span class="proj-metric-label">Total Return</span></div>
            <div class="proj-metric"><span class="proj-metric-num">1,259</span><span class="proj-metric-label">Trading Days</span></div>
            <div class="proj-metric"><span class="proj-metric-num">7</span><span class="proj-metric-label">Charts Built</span></div>
          </div>
          <div class="proj-tags"><span class="proj-tag">Python</span><span class="proj-tag">Pandas</span><span class="proj-tag">Matplotlib</span><span class="proj-tag">Seaborn</span></div>
          <div class="proj-footer">
            <a href="https://github.com/Meshwa-gif/AAPL-Stock-Analysis" target="_blank" class="proj-link proj-link-primary" style="flex:1">View on GitHub →</a>
            
          </div>
        </div>
      </div>

      <!-- PROJECT 3 -->
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-num">Project 03</div>
          <div class="proj-title">Customer Churn Prediction</div>
          <div class="proj-type">SQL + Python · Machine Learning</div>
        </div>
        <div class="proj-body">
          <p class="proj-desc">SQL-powered churn analysis on 7,043 telecom customers. Logistic Regression and Random Forest models with feature importance analysis and 5 data-backed retention recommendations.</p>
          <div class="proj-metrics">
            <div class="proj-metric"><span class="proj-metric-num">0.834</span><span class="proj-metric-label">ROC-AUC Score</span></div>
            <div class="proj-metric"><span class="proj-metric-num">26.6%</span><span class="proj-metric-label">Churn Found</span></div>
            <div class="proj-metric"><span class="proj-metric-num">42.7%</span><span class="proj-metric-label">M-t-M Churn</span></div>
          </div>
          <div class="proj-tags"><span class="proj-tag">SQL</span><span class="proj-tag">scikit-learn</span><span class="proj-tag">Python</span><span class="proj-tag">Random Forest</span></div>
          <div class="proj-footer">
            <a href="https://github.com/Meshwa-gif/Customer-Churn-Prediction" target="_blank" class="proj-link proj-link-primary" style="flex:1">View on GitHub →</a>
            
          </div>
        </div>
      </div>

      <!-- PROJECT 4 -->
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-num">Project 04</div>
          <div class="proj-title">IBM HR Analytics Dashboard</div>
          <div class="proj-type">Tableau · HR Analytics</div>
        </div>
        <div class="proj-body">
          <p class="proj-desc">Tableau dashboard analyzing 1,470 IBM employees across 6 interactive panels — attrition by department, age group, income, job satisfaction, and marital status with KPI cards.</p>
          <div class="proj-metrics">
            <div class="proj-metric"><span class="proj-metric-num">16.1%</span><span class="proj-metric-label">Attrition Rate</span></div>
            <div class="proj-metric"><span class="proj-metric-num">27.9%</span><span class="proj-metric-label">Under-30 Churn</span></div>
            <div class="proj-metric"><span class="proj-metric-num">$6,503</span><span class="proj-metric-label">Avg Income</span></div>
          </div>
          <div class="proj-tags"><span class="proj-tag">Tableau</span><span class="proj-tag">HR Analytics</span><span class="proj-tag">Dashboard</span><span class="proj-tag">Data Viz</span></div>
          <div class="proj-footer">
            <a href="https://github.com/Meshwa-gif/IBM-HR-Analytics-Tableau" target="_blank" class="proj-link proj-link-primary" style="flex:1">View on GitHub →</a>
            
          </div>
        </div>
      </div>

      <!-- PROJECT 5 -->
      <div class="proj-card">
        <div class="proj-top">
          <div class="proj-num">Project 05</div>
          <div class="proj-title">E-Commerce KPI Report</div>
          <div class="proj-type">SQL + Python · E-Commerce Analytics</div>
        </div>
        <div class="proj-body">
          <p class="proj-desc">Analyzed 99,441 real orders from Brazil's Olist platform using SQL JOINs across 5 relational tables. Revenue trends, fulfillment rates, payment analysis, geographic distribution, and review scores.</p>
          <div class="proj-metrics">
            <div class="proj-metric"><span class="proj-metric-num">$15.5M</span><span class="proj-metric-label">Total Revenue</span></div>
            <div class="proj-metric"><span class="proj-metric-num">97%</span><span class="proj-metric-label">Fulfillment Rate</span></div>
            <div class="proj-metric"><span class="proj-metric-num">4.15★</span><span class="proj-metric-label">Avg Review</span></div>
          </div>
          <div class="proj-tags"><span class="proj-tag">SQL</span><span class="proj-tag">Python</span><span class="proj-tag">Matplotlib</span><span class="proj-tag">Excel Export</span></div>
          <div class="proj-footer">
            <a href="https://github.com/Meshwa-gif/Ecommerce-Olist-SQL-Analysis" target="_blank" class="proj-link proj-link-primary" style="flex:1">View on GitHub →</a>
            
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section class="exp-section" id="experience">
  <div class="section-inner">
    <div class="section-label">Work history</div>
    <h2 class="section-title">Experience</h2>
    <p class="section-sub">Building real analytics systems across supply chain, finance, and audit</p>
    <div class="exp-list">
      <div class="exp-card">
        <div class="exp-left">
          <div class="exp-dot"></div>
          <div class="exp-dates">Apr 2025<br>— Mar 2026</div>
        </div>
        <div>
          <div class="exp-title">Data Analyst Intern</div>
          <div class="exp-company">TRM Enterprise · Charleston, WV</div>
          <ul class="exp-bullets">
            <li>Built Power BI dashboard suite tracking 10+ supply chain KPIs — predictive delay flags cut operational delays by 15%</li>
            <li>Engineered ETL pipelines in Python & SQL reducing manual reporting time by 60% and accelerating stakeholder decisions by 2 days</li>
            <li>Translated ERP data into executive-facing ad-hoc analyses and C-suite forecasting reports</li>
          </ul>
        </div>
      </div>
      <div class="exp-card">
        <div class="exp-left">
          <div class="exp-dot"></div>
          <div class="exp-dates">Aug 2024<br>— Mar 2025</div>
        </div>
        <div>
          <div class="exp-title">Student Assistant, Data Analytics</div>
          <div class="exp-company">University of Charleston · Charleston, WV</div>
          <ul class="exp-bullets">
            <li>Automated 8+ recurring financial reports using Python & SQL — saved 5+ hrs/week (~$6,500/yr) and eliminated recurring data errors</li>
            <li>Built Tableau dashboards surfacing cost driver trends that contributed to a 10% institutional cost reduction</li>
            <li>Designed data governance frameworks standardizing inputs from 3+ source systems</li>
          </ul>
        </div>
      </div>
      <div class="exp-card">
        <div class="exp-left">
          <div class="exp-dot"></div>
          <div class="exp-dates">Jan 2023<br>— Jun 2024</div>
        </div>
        <div>
          <div class="exp-title">Financial Data Analyst</div>
          <div class="exp-company">Ajay Vansjalia & Associates · Gujarat, India</div>
          <ul class="exp-bullets">
            <li>Engineered SQL-based financial data pipelines auditing transaction records — reduced reporting errors by 30%</li>
            <li>Built R-based statistical modeling and risk modeling scripts improving audit efficiency by 25%</li>
            <li>Led data integrity validation during cross-functional ERP migration maintaining full audit continuity</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section class="certs-section" id="certs">
  <div class="section-inner">
    <div class="section-label" style="color:var(--blue-accent)">Credentials</div>
    <h2 class="section-title" style="color:var(--white);margin-bottom:2rem">Certifications</h2>
    <div class="certs-grid">
      <div class="cert-card"><div class="cert-icon">🏅</div><div class="cert-name">Deloitte Australia — Technology Job Simulation</div><div class="cert-issuer">Deloitte</div></div>
      <div class="cert-card"><div class="cert-icon">📊</div><div class="cert-name">Foundations of Data Science</div><div class="cert-issuer">Google / Coursera</div></div>
      <div class="cert-card"><div class="cert-icon">🗄️</div><div class="cert-name">SQL for Any IT Professional: Unit 1</div><div class="cert-issuer">Coursera</div></div>
      <div class="cert-card"><div class="cert-icon">🔍</div><div class="cert-name">Deloitte Australia — Data Analytics Job Simulation</div><div class="cert-issuer">Deloitte</div></div>
      <div class="cert-card"><div class="cert-icon">📈</div><div class="cert-name">Foundations: Data, Data, Everywhere</div><div class="cert-issuer">Google</div></div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="contact-inner">
    <div class="section-label" style="text-align:center">Get in touch</div>
    <h2 class="section-title">Let's build something from your data 🚀</h2>
    <p style="font-size:15px;color:var(--text-muted);margin-top:.5rem">Open to full-time Data Analyst and Business Intelligence Analyst roles in the US — remote or hybrid.</p>
    <div class="contact-btns">
      <a href="mailto:meshwapatel2508@gmail.com" class="btn-primary">✉ Email me</a>
      <a href="https://www.linkedin.com/in/meshwapatel-2b24a8385" target="_blank" class="btn-outline">🔗 LinkedIn</a>
      <a href="https://github.com/Meshwa-gif" target="_blank" class="btn-outline">💻 GitHub</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>Built by Meshwa Patel · Data Analyst · Charleston, WV · 2026</p>
</footer>

</body>
</html>
