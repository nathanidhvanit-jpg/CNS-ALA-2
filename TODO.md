# Product outcomes and acceptance criteria

## [x] 1. Homepage, navigation, and responsive cybersecurity presentation
- The homepage title is **Malware Behavior Simulator** and its subtitle is **Safe and Controlled Simulation of Virus, Worm, and Trojan Behavior**.
- Include a short description explaining that this is an educational simulator; three malware cards (Virus, Worm, Trojan); **Start Simulation**, **Learn More**, and **View Report** actions; and the clear notice **“Educational simulation only — no real malware is executed.”**
- Add top navigation with **Home | Simulator | Comparison | Report | Prevention | About**.
- Use a professional dark cybersecurity dashboard with modern cards, blue/cyan accents, subtle animations, terminal-style logs, clean typography, and responsive desktop, tablet, and mobile layouts. Make the result screenshot-friendly and polished for a GMIU college practical submission.

## [x] 2. Interactive virtual simulation dashboard
- Provide Virus, Worm, and Trojan selectors; simulation speed choices Slow / Normal / Fast; and Start, Pause, Reset, and Stop Simulation controls.
- Show exactly five safe virtual nodes: Computer A, Computer B, Computer C, Computer D, and Computer E. All nodes and connections shown by the website are fictional objects represented only in application memory.
- Demonstrate behavior using virtual data only. Controls update only the in-page simulation state.

## [x] 3. Virus simulation
- When Virus is selected, show one infected virtual computer at the start. Simulate replication only inside the virtual environment, changing virtual node states from “Safe” to “Infected”.
- Display Infected Nodes, Replication Count, and Simulation Time.
- The log supports representative timestamped events: simulation started; Virtual Computer A infected; simulated replication detected; Virtual Computer B marked infected.
- Do not create, modify, delete, or infect real files.

## [x] 4. Worm simulation
- Visually animate spread between connected virtual nodes, with a predefined example such as **Computer A → Computer B → Computer C → Computer D**.
- Show the number of virtual nodes, the number of simulated connections, spread count, and current simulation status.
- Use only predefined virtual nodes; do not make real network connections or send network packets.

## [x] 5. Trojan simulation
- Show a Trojan disguised as a harmless, fictional application such as **“Free Game.exe”**; show the simulated user launching the application, a warning, and virtual Trojan behavior detected.
- Display the disguised application, user action, simulated malicious behavior, and detection status.
- Do not execute actual executable files or perform real system actions.

## [x] 6. Live log, statistics, and chart
- Provide a terminal-style panel showing simulated timestamped events in real time, including initialization, virtual-environment creation, virtual node creation, selected simulation start, virtual replication, node B marked infected, and safe completion as applicable.
- Include a **Clear Log** button.
- Show statistics for Total Virtual Nodes, Simulated Infections, Replication Events, Detection Events, and Simulation Duration.
- Include a simple chart showing simulated spread over time.

## [x] 7. Malware comparison
- Include a comparison table with Feature, Virus, Worm, and Trojan columns and the following values:
  - Requires host file: Virus **Yes**; Worm **No**; Trojan **Usually disguised as legitimate software**.
  - Self-replication: Virus **Yes**; Worm **Yes**; Trojan **No**.
  - Network spreading: Virus **Usually limited**; Worm **Common**; Trojan **Not inherent**.
  - Disguise: Virus **Sometimes**; Worm **Usually no**; Trojan **Yes**.
  - Main concept: Virus **Replication**; Worm **Network propagation**; Trojan **Deception**.

## [x] 8. Educational report
- Provide a **Generate Report** section containing Introduction, Objective, Virus behavior, Worm behavior, Trojan behavior, Simulation methodology, Observations, Impact of malware, Prevention methods, and Conclusion.
- Display the report on screen and provide a **Print/Save Report** option.

## [x] 9. Prevention and About education
- Explain and recommend: keep operating systems updated; use reputable antivirus/security software; avoid unknown downloads; do not open suspicious attachments; use strong passwords and multi-factor authentication; keep regular backups; learn to identify phishing and suspicious applications.
- About explains the educational, isolated, fictional-only nature of the college-project simulator.

## [x] 10. Non-negotiable safety and completion behavior
- The website is a simulation only. Never access or modify real files; delete or encrypt files; execute malware; create persistence; scan real networks; send network packets; spread software; access user credentials; collect personal information; disable security software; or run shell/system commands.
- All computers, files, applications, infections, and network connections shown are fictional objects represented only in application memory.
- The application does not make real network connections for simulations and does not perform real system actions.
- At the end of the simulation, display exactly: **“Simulation completed successfully. No real files, devices, networks, or systems were affected.”**
