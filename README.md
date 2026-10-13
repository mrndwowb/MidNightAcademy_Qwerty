# MidNightAcademy_Qwerty
## Project Overview

The Midnight Academy is an interactive browser‑based experience built as a single‑page HTML‑CSS‑JavaScript application. It frames academic disciplines as magical schools: Graph Theory (Thread‑Weaver), Thermodynamics (Heat‑Keeper), and Sociolinguistics (Echo‑Shaper). Users select up to two schools, cast knowledge‑grounded spells, observe discipline‑specific outputs, unlock cross‑disciplinary insights, and run challenge trials. All state and experiment logs are stored locally inside the browser.

This project fulfils competition requirements: fully interactive and **demonstrable on‑site**. It runs locally without internet access, so live demonstration on presentation day is reliable.

## How to Run

1. Download the `index.html` source file.
2. Open the file in Visual Studio Code.
3. Launch via the Live Server extension.
4. A browser window will open showing the opening intro screen.
5. Click `Enter the Academy (Dream)` to enter the apprentice workspace.

> 
> No build tools, no backend server, no external API calls required. Works offline for on‑site demo.
>
## Core Features

- Intro landing screen that transitions to main workspace
- Magic school selection (maximum 2 schools enforced by application logic)
- Dynamically rendered spell buttons based on selected schools
- Spell‑casting outputs with success / fail visual animations
- Cross‑discovery bonus text when two schools are active together
- Challenge trial puzzle for guided exploration
- Local‑browser experiment log: auto‑saves history, supports clear‑log and copy‑to‑clipboard
- Responsive layout for classroom laptop demonstration

Key Design Decisions & Technical Trade‑offs
1. **Single‑page application (one HTML file only)**
   - Decision: Combine HTML, CSS, JavaScript in one file instead of splitting across multiple pages or separate source files.
   - Trade‑off:
     - Pros: Extremely portable for on‑site demonstration. Zero dependency setup risk. No broken file‑path issues during presentation. Simple submission as one file.
     - Cons: Source file becomes longer; cannot split code for large‑scale future expansion. Suitable for this competition‑scale prototype.
2.**LocalStorage for experiment log, no backend database**

- Decision: Store user experiment history inside browser `localStorage`.
- Trade‑off:
  - Pros: Works fully offline. No server maintenance, no network dependency for demo day. User records persist after page refresh.
  - Cons: Data only stays on the local device; cannot sync across different computers. Fits the scope of a classroom interactive prototype.
 
3. **Enforce maximum of two magic schools via front‑end JavaScript logic**

- Decision: Apply constraint logic inside client‑side code instead of using backend validation.
- Trade‑off:
  - Pros: Immediate user feedback without network delay. Clear rule warning text shown to users.
  - Cons: Front‑end rules can be bypassed by advanced users modifying browser code. For this demo‑focused project, user experience takes priority over anti‑tamper hardening.
 
  4. **Knowledge‑based simulated spell outcomes, no external AI model calls**

- Decision: Hard‑code spell logic and results based on domain knowledge (graph theory rules, thermodynamics constraints, sociolinguistic observations). Outcomes use controlled randomness for partial success/failure simulation.
- Trade‑off:
  - Pros: 100% offline execution. Predictable behaviour for on‑site demo; no risk of AI API outage or rate‑limit failures during presentation.
  - Cons: Responses are pre‑authored rather than open‑ended generative outputs. Project prioritises stable demonstrability over unbounded free text generation.
 
  5. **CSS‑only animations for success / fail feedback**

- Decision: Use CSS keyframe animations instead of JavaScript animation libraries.
- Trade‑off:
  - Pros: Lightweight, no third‑party library dependencies. Reliable across standard browsers.
  - Cons: Limited custom animation complexity. Matches prototype needs.
 
  ## AI Usage Statement

This project **does not call or integrate any external AI model API** for runtime features. All spell logic, texts, world‑building descriptions and interface content are manually authored.

Some phrasing and structural suggestions for source‑code refinement were assisted by AI tools. All creative settings, school names, character‑free world concept are original. No characters, names, plot settings are copied from existing books, games or media. All AI‑assisted assets satisfy originality requirements for this submission.

