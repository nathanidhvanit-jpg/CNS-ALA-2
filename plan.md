# Malware Behavior Simulator — Implementation Plan

## Product and implementation approach

Build a polished, responsive, single-page educational dashboard for GMIU's college practical project. It presents Virus, Worm, and Trojan concepts through deterministic, fictional simulations. The simulator's entire data model consists of hard-coded virtual node records, virtual connection records, counters, and event entries held in browser memory. All state resets when the page is reloaded; there is no API, database, account, telemetry, local storage, file access, system command, executable launch, network scan, packet transmission, external service call, or peer-to-peer behavior. A small dependency-free Node static file server exists only to serve the website in Preview; it exposes no simulation API. A dependency-free build script copies the static website into `dist/` for a possible static build.

The one-page interface provides Home, Simulator, Comparison, Report, Prevention, and About anchor navigation. The simulator includes Virus/Worm/Trojan mode selection, Slow/Normal/Fast speed, Start/Pause/Reset/Stop controls, five fixed virtual computers A–E, Safe → Infected virtual states, virtual-only counters, elapsed wall-clock time, timeline/chart, and a timestamped terminal log. Each mode has a distinct safe teaching visualization: in-memory replication across nodes for Virus, four predefined in-memory virtual edges for Worm, and an explicitly fictional “Free Game.exe” deception flow for Trojan. The report is rendered in-page and printed/saved only through the browser's print dialog. The exact required safety notice and simulation-completion statement remain visible.

## Design direction

- **Design Movement:** Contemporary security operations interface with restrained terminal-editorial detailing.
- **Core Principles:** Evidence-like clarity; visibly safe-by-design interactions; high information density with generous separation; responsive accessibility.
- **Color Philosophy:** Deep ink and midnight-blue surfaces convey a contained control room; a distinctive aqua-cyan identifies safe activity and interactive focus; subdued amber and coral distinguish warnings and simulated risk without implying a real threat.
- **Layout Paradigm:** Asymmetric operations-console composition: compact vertical navigation/identity, a wide working canvas, and a narrow telemetry rail on desktop; these regions stack into a clear reading order on mobile. Sections are arranged as a purposeful dashboard rather than a uniform centered card grid.
- **Signature Elements:** A custom CSS hex-shield `M//` mark; slim cyan instrument rules and connected-node motifs; a terminal-inspired event stream paired with status pills.
- **Interaction Philosophy:** Controls change only fictional in-memory state. Mode and speed selection are explicit; pause/reset/stop visibly update status; reduced-motion preferences are respected.
- **Animation:** Short, subtle node pulse and connection-draw transitions communicate simulated events; avoid flashing, rapid movement, and motion when `prefers-reduced-motion` is enabled.
- **Typography System:** Clean system sans-serif for headings and body, paired with a system monospace stack for timestamps, counters, node IDs, and logs; use restrained uppercase labels and a strong hierarchy.
- **Brand Essence:** A safe, browser-only teaching lab that makes malware behavior understandable without running malware — precise, calm, educational.
- **Brand Voice:** Clear, technical, reassuring. Examples: “Observe the pattern. Nothing leaves this sandbox.” “Every event is virtual; your device stays untouched.”
- **Wordmark & Logo:** A small outlined hexagonal shield containing a custom `M//` glyph, followed by a distinctive two-line wordmark.
- **Signature Brand Color:** Aqua-cyan `#63E6D2`.

## Architecture and project structure

- `package.json` — dependency-free `start` and `build` scripts.
- `server.mjs` — minimal Node static-file server for Preview; serves only committed website assets and has no simulator/API endpoints.
- `build.mjs` — reproducibly copies `public/` to `dist/` using Node built-ins.
- `public/manus-routes.json` — required route declaration for the single page `/`.
- `public/index.html` — semantic one-page shell, navigation, dashboard sections, status live regions, report, and safety statements.
- `public/assets/styles.css` — responsive visual system, dashboard composition, state visuals, print rules, and reduced-motion support.
- `public/assets/app.js` — fictional in-memory simulator state machine, timer, deterministic event log, chart rendering, controls, report generation/print, and safe DOM updates. No browser persistence or network calls.

**Serving and dependencies:** Frontend is static HTML/CSS/vanilla JavaScript; there are no third-party packages or external runtime resources. The Node server is solely the Preview/static-site host and listens on the configured port. The application itself has no backend, database, authentication, external API, outbound requests, or persisted data. Static build output is `dist/`.

## Required behavior and constraints

The homepage must use the title “Malware Behavior Simulator”, subtitle “Safe and Controlled Simulation of Virus, Worm, and Trojan Behavior”, explain the educational purpose, show Virus/Worm/Trojan cards, provide Start Simulation / Learn More / View Report actions, and clearly display “Educational simulation only — no real malware is executed.” The navigation labels are Home | Simulator | Comparison | Report | Prevention | About.

The simulator has Virus/Worm/Trojan selection, Slow/Normal/Fast speed, Start/Pause/Reset/Stop Simulation, and exactly five predefined fictional nodes Computer A–E. Virus begins with one infected virtual computer and changes node labels Safe → Infected while displaying infected nodes, replication count, and simulation time, with representative timestamped start, Computer A infected, simulated replication, and Computer B marked infected events. Worm displays and animates a predefined virtual chain such as Computer A → Computer B → Computer C → Computer D, tracking virtual-node count, virtual-connection count, spread count, and status. Trojan uses fictional “Free Game.exe” to show a simulated launch, warning, virtual Trojan behavior detected, and detection state without launching a file. The live terminal log timestamps simulated events and includes Clear Log. Statistics include total virtual nodes, simulated infections, replication events, detection events, and duration, with a spread-over-time chart. The comparison table preserves the user's requested Virus/Worm/Trojan values for host-file dependency, self-replication, network spreading, disguise, and main concept. The educational report has Introduction, Objective, Virus behavior, Worm behavior, Trojan behavior, Simulation methodology, Observations, Impact of malware, Prevention methods, and Conclusion, displayed on screen with Print/Save Report. Prevention advice covers OS updates, reputable antivirus/security software, unknown downloads, suspicious attachments, strong passwords and MFA, regular backups, phishing, and suspicious applications. About explains the fictional-only methodology and college-project context.

Never access or modify real files; delete or encrypt files; execute malware or executable files; create persistence; scan real networks; send network packets; spread software; access credentials; collect personal information; disable security software; or run shell/system commands. All computers, files, applications, infections, and connections are fictional objects held only in application memory. End a completed simulation with exactly: “Simulation completed successfully. No real files, devices, networks, or systems were affected.”
