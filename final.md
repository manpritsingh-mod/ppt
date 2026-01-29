<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Internship Review | Manprit Singh Panesar</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap"
        rel="stylesheet">
    <style>
        :root {
            --bg: #0a0a0f;
            --card: rgba(255, 255, 255, 0.03);
            --border: rgba(255, 255, 255, 0.08);
            --blue: #3b82f6;
            --purple: #8b5cf6;
            --green: #10b981;
            --orange: #f59e0b;
            --text: #ffffff;
            --muted: #94a3b8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: var(--bg);
            color: var(--text);
            overflow: hidden;
        }

        .bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: radial-gradient(ellipse at 20% 20%, rgba(59, 130, 246, 0.12) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 80%, rgba(139, 92, 246, 0.08) 0%, transparent 50%);
        }

        .slide {
            width: 100vw;
            height: 100vh;
            position: absolute;
            display: none;
            padding: 45px 60px;
            opacity: 0;
            transition: opacity 0.4s, transform 0.4s;
        }

        .slide.active {
            display: flex;
            flex-direction: column;
            opacity: 1;
        }

        .badge {
            display: inline-block;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .q1 {
            background: rgba(59, 130, 246, 0.15);
            border: 1px solid rgba(59, 130, 246, 0.3);
            color: #60a5fa;
        }

        .q2 {
            background: rgba(139, 92, 246, 0.15);
            border: 1px solid rgba(139, 92, 246, 0.3);
            color: #a78bfa;
        }

        .q3 {
            background: rgba(16, 185, 129, 0.15);
            border: 1px solid rgba(16, 185, 129, 0.3);
            color: #34d399;
        }

        .q4 {
            background: rgba(245, 158, 11, 0.15);
            border: 1px solid rgba(245, 158, 11, 0.3);
            color: #fbbf24;
        }

        h1 {
            font-size: 3rem;
            font-weight: 800;
            letter-spacing: -1px;
        }

        h2 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 25px;
        }

        h3 {
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 14px;
        }

        .card {
            background: var(--card);
            backdrop-filter: blur(20px);
            border: 1px solid var(--border);
            border-radius: 14px;
            padding: 20px;
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            flex: 1;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px;
        }

        .grid-5 {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 14px;
            flex: 1;
        }

        .obj {
            border-top: 3px solid var(--blue);
        }

        .obj h3 {
            color: #60a5fa;
        }

        .ach {
            border-top: 3px solid var(--green);
        }

        .ach h3 {
            color: #34d399;
        }

        .learn {
            border-top: 3px solid var(--purple);
        }

        .learn h3 {
            color: #a78bfa;
        }

        .chal {
            border-top: 3px solid var(--orange);
        }

        .chal h3 {
            color: #fbbf24;
        }

        .arch {
            border-top: 3px solid #06b6d4;
        }

        .arch h3 {
            color: #22d3ee;
        }

        .pt {
            padding: 8px 0;
            color: var(--muted);
            font-size: 0.82rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.03);
            line-height: 1.4;
        }

        .pt:last-child {
            border-bottom: none;
        }

        .nav {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
            z-index: 100;
        }

        .nav button {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            color: #fff;
            padding: 10px 22px;
            border-radius: 25px;
            cursor: pointer;
            font-family: inherit;
            font-size: 0.8rem;
            transition: 0.3s;
        }

        .nav button:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        .progress {
            position: fixed;
            top: 0;
            left: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--blue), var(--purple));
            transition: width 0.3s;
        }

        .indicator {
            position: fixed;
            bottom: 25px;
            right: 50px;
            color: var(--muted);
            font-size: 0.8rem;
        }

        .title-slide {
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .title-slide h1 {
            font-size: 3.5rem;
            background: linear-gradient(135deg, #fff, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .meta {
            display: flex;
            gap: 35px;
            color: var(--muted);
            font-size: 0.8rem;
            margin-top: 35px;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 35px;
            flex: 1;
            align-items: center;
        }

        .info-row {
            display: flex;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            font-size: 0.9rem;
        }

        .info-label {
            width: 130px;
            color: var(--muted);
            font-weight: 500;
        }

        .profile {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 18px;
        }

        .avatar {
            width: 130px;
            height: 130px;
            border-radius: 14px;
            background: linear-gradient(135deg, var(--blue), var(--purple));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            justify-content: center;
        }

        .tag {
            padding: 7px 12px;
            border-radius: 18px;
            font-size: 0.75rem;
            background: rgba(139, 92, 246, 0.1);
            border: 1px solid rgba(139, 92, 246, 0.25);
            color: #a78bfa;
        }

        .roadmap {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 14px;
            flex: 1;
        }

        .rm-card {
            padding: 20px;
            border-radius: 14px;
        }

        .rm-card.q1-c {
            background: linear-gradient(180deg, rgba(59, 130, 246, 0.1), transparent);
            border: 1px solid rgba(59, 130, 246, 0.2);
        }

        .rm-card.q2-c {
            background: linear-gradient(180deg, rgba(139, 92, 246, 0.1), transparent);
            border: 1px solid rgba(139, 92, 246, 0.2);
        }

        .rm-card.q3-c {
            background: linear-gradient(180deg, rgba(16, 185, 129, 0.1), transparent);
            border: 1px solid rgba(16, 185, 129, 0.2);
        }

        .rm-card.q4-c {
            background: linear-gradient(180deg, rgba(245, 158, 11, 0.1), transparent);
            border: 1px solid rgba(245, 158, 11, 0.2);
        }

        .rm-header {
            font-size: 0.75rem;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .rm-card.q1-c .rm-header {
            color: #60a5fa;
        }

        .rm-card.q2-c .rm-header {
            color: #a78bfa;
        }

        .rm-card.q3-c .rm-header {
            color: #34d399;
        }

        .rm-card.q4-c .rm-header {
            color: #fbbf24;
        }

        .rm-title {
            font-size: 1rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .rm-list {
            list-style: none;
            color: var(--muted);
            font-size: 0.8rem;
        }

        .rm-list li {
            padding: 3px 0;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px;
            margin-bottom: 25px;
        }

        .stat {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 14px;
            padding: 24px;
            text-align: center;
        }

        .stat-icon {
            font-size: 1.8rem;
            margin-bottom: 8px;
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 800;
        }

        .stat-value.blue {
            color: #60a5fa;
        }

        .stat-value.green {
            color: #34d399;
        }

        .stat-value.purple {
            color: #a78bfa;
        }

        .stat-value.orange {
            color: #fbbf24;
        }

        .stat-label {
            color: var(--muted);
            font-size: 0.8rem;
            margin-top: 4px;
        }

        .thankyou {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #60a5fa, #a78bfa, #34d399);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        pre {
            background: #0d0d12;
            border-radius: 10px;
            padding: 16px;
            font-size: 0.65rem;
            overflow: auto;
            color: #e2e8f0;
            line-height: 1.5;
            margin-top: 10px;
        }

        .flow {
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            margin: 15px 0;
        }

        .flow-step {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.2), rgba(139, 92, 246, 0.2));
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 12px 18px;
            border-radius: 10px;
            text-align: center;
            min-width: 100px;
        }

        .flow-step .num {
            font-size: 1.2rem;
        }

        .flow-step .lbl {
            font-weight: 600;
            font-size: 0.8rem;
        }

        .flow-arrow {
            color: var(--blue);
            font-size: 1rem;
        }
    </style>
</head>

<body>
    <div class="bg"></div>
    <div class="progress" id="progress"></div>

    <!-- Slide 1: Title -->
    <div class="slide title-slide active">
        <span class="badge"
            style="background:rgba(255,255,255,0.05); border-color:rgba(255,255,255,0.1); color:#fff;">Q1 FY'25 — Q4
            FY'26</span>
        <h1>INTERNSHIP</h1>
        <p style="font-size:1.1rem; color:var(--muted); margin:12px 0;">Building Enterprise CI/CD Solutions</p>
        <p style="font-size:1.4rem; font-weight:600;">Manprit Singh Panesar</p>
        <div class="meta">
            <span>👨‍💼 Manager: Gautom Dutta</span>
            <span>🏗️ Architect: Sunil Kumar EK</span>
            <span>🎯 Mentor: Viresh Hiremath</span>
        </div>
    </div>

    <!-- Slide 2: About Me -->
    <div class="slide">
        <h2>About Me</h2>
        <div class="about-grid">
            <div class="card">
                <div class="info-row"><span class="info-label">Role</span><span>Intern</span></div>
                <div class="info-row"><span class="info-label">Hometown</span><span>Jamshedpur, Jharkhand</span></div>
                <div class="info-row"><span class="info-label">Education</span><span>B.Tech (CSE), Arka Jain
                        University</span></div>
                <div class="info-row"><span class="info-label">Skills</span><span>Java, Spring Boot, CI/CD, Jenkins,
                        Docker</span></div>
                <div class="info-row"><span class="info-label">Tech Interest</span><span>CI/CD Automation, Backend
                        Development</span></div>
                <div class="info-row" style="border:none;"><span class="info-label">Joined</span><span>14th May,
                        2025</span></div>
            </div>
            <div class="profile">
                <div class="avatar">👨‍💻</div>
                <p style="color:var(--muted); font-size:0.8rem;">Beyond Technology</p>
                <div class="tags">
                    <span class="tag">🎨 Art & Design</span>
                    <span class="tag">✈️ Travel</span>
                    <span class="tag">🏸 Badminton</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Slide 3: Roadmap -->
    <div class="slide">
        <h2>Internship Roadmap</h2>
        <div class="roadmap">
            <div class="rm-card q1-c">
                <div class="rm-header">📚 Q1 FY'25</div>
                <div class="rm-title">Foundation & POC 1</div>
                <ul class="rm-list">
                    <li>• Jenkins & Docker fundamentals</li>
                    <li>• Groovy & Python scripting</li>
                    <li>• POC 1: Repository Maintenance</li>
                </ul>
            </div>
            <div class="rm-card q2-c">
                <div class="rm-header">🔧 Q2 FY'25</div>
                <div class="rm-title">UnifiedCI Core</div>
                <ul class="rm-list">
                    <li>• Shared Library architecture</li>
                    <li>• Java & Python pipelines</li>
                    <li>• POC 2: UnifiedCI</li>
                </ul>
            </div>
            <div class="rm-card q3-c">
                <div class="rm-header">🚀 Q3 FY'25</div>
                <div class="rm-title">React + AI/ML</div>
                <ul class="rm-list">
                    <li>• React/React-Native support</li>
                    <li>• Jenkins MCP exploration</li>
                    <li>• AI-assisted CI research</li>
                </ul>
            </div>
            <div class="rm-card q4-c">
                <div class="rm-header">📱 Q4 FY'26</div>
                <div class="rm-title">Mobile CI/CD</div>
                <ul class="rm-list">
                    <li>• Android CI/CD pipeline</li>
                    <li>• Play Store deployment</li>
                    <li>• AI/ML integration</li>
                </ul>
            </div>
        </div>
    </div>

    <!-- Slide 4: Q1 Overview -->
    <div class="slide">
        <span class="badge q1">Q1 FY'25</span>
        <h2>Foundation & POC 1</h2>
        <div class="grid-5">
            <div class="card obj">
                <h3>🎯 Objective</h3>
                <div class="pt">Develop foundational CI/CD skills</div>
                <div class="pt">Master Jenkins pipeline development</div>
                <div class="pt">Automate repository maintenance</div>
            </div>
            <div class="card ach">
                <h3>✅ Achievements</h3>
                <div class="pt">Completed onboarding & KT</div>
                <div class="pt">Built shared-library for email & XLS</div>
                <div class="pt">Delivered POC 1: Automated PR cleanup</div>
            </div>
            <div class="card learn">
                <h3>📚 Learnings</h3>
                <div class="pt">Jenkins pipelines & Docker</div>
                <div class="pt">Groovy & Python scripting</div>
                <div class="pt">IT communication protocols</div>
                <div class="pt">Access request workflows</div>
            </div>
            <div class="card chal">
                <h3>⚡ Challenges</h3>
                <div class="pt">GitHub access onboarding</div>
                <div class="pt">Linux PC setup for Jenkins</div>
                <div class="pt">SWAN2 network access</div>
            </div>
            <div class="card arch">
                <h3>🏗️ Architecture</h3>
                <div class="pt" style="font-size:0.75rem;">Job Trigger → Analyze PRs → Label Stale → Auto-Close → Delete
                    Branches</div>
                <div class="pt" style="margin-top:8px;">4-stage automated flow</div>
                <div class="pt">GitHub API integration</div>
            </div>
        </div>
    </div>

    <!-- Slide 5: Q2 Overview -->
    <div class="slide">
        <span class="badge q2">Q2 FY'25</span>
        <h2>UnifiedCI Core (POC 2)</h2>
        <div class="grid-5">
            <div class="card obj">
                <h3>🎯 Objective</h3>
                <div class="pt">Build unified Jenkins Shared Library</div>
                <div class="pt">Support Java & Python pipelines</div>
                <div class="pt">Standardize CI/CD across org</div>
            </div>
            <div class="card ach">
                <h3>✅ Achievements</h3>
                <div class="pt">Designed & delivered UnifiedCI</div>
                <div class="pt">Auto-detection for languages</div>
                <div class="pt">Maven/Gradle & Python support</div>
            </div>
            <div class="card learn">
                <h3>📚 Learnings</h3>
                <div class="pt">Shared Library architecture</div>
                <div class="pt">JUnit, pytest frameworks</div>
                <div class="pt">Cross-team collaboration</div>
                <div class="pt">Documentation best practices</div>
            </div>
            <div class="card chal">
                <h3>⚡ Challenges</h3>
                <div class="pt">Linux PC space issue</div>
                <div class="pt">New PC provisioned</div>
                <div class="pt">Monorepo detection edge cases</div>
            </div>
            <div class="card arch">
                <h3>🏗️ Architecture</h3>
                <div class="pt" style="font-size:0.75rem;">vars/ (pipeline entry) → src/ (core logic) → templates</div>
                <div class="pt" style="margin-top:8px;">Modular plugin system</div>
                <div class="pt">YAML-based configuration</div>
            </div>
        </div>
    </div>

    <!-- Slide 6: Q3 Overview -->
    <div class="slide">
        <span class="badge q3">Q3 FY'25</span>
        <h2>React Extension + AI/ML</h2>
        <div class="grid-5">
            <div class="card obj">
                <h3>🎯 Objective</h3>
                <div class="pt">Extend UnifiedCI for React</div>
                <div class="pt">Explore AI/ML for CI automation</div>
                <div class="pt">Research Jenkins MCP</div>
            </div>
            <div class="card ach">
                <h3>✅ Achievements</h3>
                <div class="pt">React/React-Native support added</div>
                <div class="pt">Jenkins MCP exploration done</div>
                <div class="pt">AI/ML use cases documented</div>
            </div>
            <div class="card learn">
                <h3>📚 Learnings</h3>
                <div class="pt">React ecosystem (npm, Jest)</div>
                <div class="pt">Model Context Protocol</div>
                <div class="pt">Presenting to stakeholders</div>
                <div class="pt">Research & documentation</div>
            </div>
            <div class="card chal">
                <h3>⚡ Challenges</h3>
                <div class="pt">Cross-language compatibility</div>
                <div class="pt">Balancing dev with research</div>
                <div class="pt">MCP architecture complexity</div>
            </div>
            <div class="card arch">
                <h3>🏗️ Architecture</h3>
                <div class="pt" style="font-size:0.75rem;">LLM ↔ MCP Server ↔ Jenkins API</div>
                <div class="pt" style="margin-top:8px;">AI-assisted log analysis</div>
                <div class="pt">Smart failure detection</div>
            </div>
        </div>
    </div>

    <!-- Slide 7: Q4 Overview -->
    <div class="slide">
        <span class="badge q4">Q4 FY'26</span>
        <h2>Mobile CI/CD + AI/ML</h2>
        <div class="grid-5">
            <div class="card obj">
                <h3>🎯 Objective</h3>
                <div class="pt">Build Android CI/CD with Docker</div>
                <div class="pt">Enable Play Store deployment</div>
                <div class="pt">Advance AI/ML integration</div>
            </div>
            <div class="card ach">
                <h3>✅ Achievements</h3>
                <div class="pt">Docker environment ready</div>
                <div class="pt">Build & test pipeline working</div>
                <div class="pt">🔄 Play Store in progress</div>
            </div>
            <div class="card learn">
                <h3>📚 Learnings</h3>
                <div class="pt">Android CI/CD patterns</div>
                <div class="pt">Fastlane deployment</div>
                <div class="pt">Independent problem solving</div>
                <div class="pt">Delivery timeline mgmt</div>
            </div>
            <div class="card chal">
                <h3>⚡ Challenges</h3>
                <div class="pt">Play Store validation</div>
                <div class="pt">Signing cert management</div>
                <div class="pt">AI model complexity</div>
            </div>
            <div class="card arch">
                <h3>🏗️ Architecture</h3>
                <div class="pt" style="font-size:0.75rem;">Jenkins → Docker Agent → Build → Deploy</div>
                <div class="pt" style="margin-top:8px;">Java 17 + Node 20 + SDK 34</div>
                <div class="pt">Fastlane + Gradle</div>
            </div>
        </div>
    </div>

    <!-- Slide 8: Architecture Deep Dive -->
    <div class="slide">
        <h2>Architecture Overview</h2>
        <div class="grid-2">
            <div class="card arch">
                <h3>🏗️ UnifiedCI Shared Library</h3>
                <pre>
┌─────────────────────────────────────────┐
│      SHARED LIBRARY REPOSITORY          │
├─────────────────────────────────────────┤
│  vars/ (Entry)       │  src/ (Logic)    │
│  • javaPipeline      │  • CommandGen    │
│  • pythonPipeline    │  • DockerMgr     │
│  • reactPipeline     │  • GitManager    │
├─────────────────────────────────────────┤
│  CORE: Build → Test → Lint → Report     │
└─────────────────────────────────────────┘
   ↓ CONSUMED BY: [Java] [Python] [React]
                </pre>
            </div>
            <div class="card" style="border-top:3px solid #fbbf24;">
                <h3 style="color:#fbbf24;">📱 Mobile CI/CD</h3>
                <pre>
┌──────────────────────────────────────┐
│         JENKINS CONTROLLER           │
│  Jenkinsfile → Shared Library        │
└──────────────────────────────────────┘
                    ↓
┌──────────────────────────────────────┐
│           DOCKER AGENT               │
│  [Java 17] [Node 20] [SDK 34]        │
│  [Fastlane] [Gradle]                 │
└──────────────────────────────────────┘
      ↓            ↓            ↓
  [Nexus]    [Play Store]    [Slack]
                </pre>
            </div>
        </div>
    </div>

    <!-- Slide 9: Key Achievements -->
    <div class="slide">
        <h2>Key Achievements</h2>
        <div class="stats">
            <div class="stat">
                <div class="stat-icon">🎯</div>
                <div class="stat-value blue">4</div>
                <div class="stat-label">POCs Delivered</div>
            </div>
            <div class="stat">
                <div class="stat-icon">🌐</div>
                <div class="stat-value purple">4</div>
                <div class="stat-label">Tech Stacks</div>
            </div>
            <div class="stat">
                <div class="stat-icon">📉</div>
                <div class="stat-value green">95%</div>
                <div class="stat-label">Code Reduction</div>
            </div>
            <div class="stat">
                <div class="stat-icon">⏱️</div>
                <div class="stat-value orange">Days→Hrs</div>
                <div class="stat-label">Setup Time</div>
            </div>
        </div>
        <div class="grid-2">
            <div class="card ach">
                <h3>✅ Delivered</h3>
                <div class="pt">POC 1: Automated Repository Maintenance</div>
                <div class="pt">POC 2: UnifiedCI for Java & Python</div>
                <div class="pt">POC 3: React Extension + AI/ML Research</div>
                <div class="pt">POC 4: Mobile CI/CD (In Progress)</div>
            </div>
            <div class="card obj">
                <h3>📄 Documentation</h3>
                <div class="pt">Architecture docs for all POCs</div>
                <div class="pt">API reference & onboarding guides</div>
                <div class="pt">Configuration schemas & examples</div>
            </div>
        </div>
    </div>

    <!-- Slide 10: Thank You -->
    <div class="slide title-slide">
        <div class="thankyou">Thank You!</div>
        <p style="font-size:1.2rem; color:var(--muted); margin-top:20px;">Questions?</p>
        <div class="meta" style="margin-top:40px;">
            <span>📧 manprit.singh@company.com</span>
            <span>💼 SISC Intern</span>
        </div>
    </div>

    <div class="nav">
        <button onclick="prevSlide()">← Previous</button>
        <button onclick="nextSlide()">Next →</button>
    </div>
    <div class="indicator"><span id="curr">1</span> / <span id="total">10</span></div>

    <script>
        let curr = 0;
        const slides = document.querySelectorAll('.slide');
        document.getElementById('total').textContent = slides.length;
        function show(n) {
            slides.forEach(s => s.classList.remove('active'));
            curr = (n + slides.length) % slides.length;
            slides[curr].classList.add('active');
            document.getElementById('curr').textContent = curr + 1;
            document.getElementById('progress').style.width = ((curr + 1) / slides.length * 100) + '%';
        }
        function nextSlide() { show(curr + 1); }
        function prevSlide() { show(curr - 1); }
        document.addEventListener('keydown', e => {
            if (e.key === 'ArrowRight' || e.key === ' ') nextSlide();
            if (e.key === 'ArrowLeft') prevSlide();
        });
    </script>
</body>

</html>
