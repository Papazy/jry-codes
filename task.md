# Terminal Portfolio — Final Specification

Build a modern, purely frontend, terminal-themed personal portfolio website using **Next.js + Tailwind CSS**, focusing on exceptional UI/UX.

---

## 1. Overall UI — macOS Terminal Illusion

* **Page Background:** A subtly blurred, dark abstract wallpaper (CSS gradient or noise texture) to give depth to the page.
* **Terminal Window:** A floating, centered window container — NOT full-screen. Fixed width (~900px), sensible max-height with internal scroll.
* **Window Header (macOS style):**
  * Three colored dots on the left: red `#ff5f57`, yellow `#febc2e`, green `#28c840`.
  * Title centered: `fajry — -zsh — 80x24`.
  * Soft `box-shadow` drop shadow behind the entire window.
* **Terminal Body:**
  * Background `#1e1e1e`, text `#d4d4d4`.
  * Monospace font: **Fira Code** (Google Fonts).
  * Custom thin scrollbar that fits the dark theme.

---

## 2. Core UX & Animations

* **Boot Sequence (on mount):** Simulate a rapid typing boot sequence before revealing the prompt:
  1. Type out `[ OK ] Booting portfolio OS...`
  2. Type out `[ OK ] Loading modules...`
  3. Type out `[ OK ] Mounting filesystem...`
  4. Brief pause → clear → show the welcome message and prompt.
* **Tab Auto-completion:** Pressing `Tab` with a partial command (e.g., `pro`) auto-completes to the first matching command (e.g., `projects`). Prevent default browser tab behavior.
* **Prompt Line:** `fajry@macbook:~$ ` — color-coded (green for user/host, cyan for path).
* **Blinking Block Cursor:** A `█` style cursor that blinks at the end of the input line.
* **Auto-Focus:** Input auto-focuses on load. Clicking anywhere on the terminal body refocuses the input (unless the user is selecting text to copy).
* **Command History:** `Arrow Up` / `Arrow Down` cycles through previously entered commands.
* **Auto-Scroll:** Terminal always scrolls to the bottom on new output.

---

## 3. Commands to Implement

| Command | Description |
|---|---|
| `help` | Lists all available commands with brief descriptions. |
| `about` | Short bio. |
| `neofetch` | Classic terminal profile with ASCII art left, info right. |
| `projects` | Lists 3 featured projects with descriptions. |
| `skills` | Full tech stack. |
| `contact` | Clickable GitHub, LinkedIn, Email links. |
| `clear` | Clears the terminal back to the welcome state. |
| *(unknown)* | `zsh: command not found: [command]` |

### Command Details

**`about`**
> Hi! I'm Fajry, a Software Engineer with a strong interest in AI Engineering, web development, and creating efficient systems. Currently working remotely from Banda Aceh.

**`neofetch`**
```
Left side: simple ASCII art logo (e.g. a stylized "F" or generic linux penguin-style art)
Right side (aligned):
  fajry@macbook
  -------------
  OS:       Portfolio OS 1.0
  Role:     Software Engineer
  Shell:    zsh
  Location: Banda Aceh, Indonesia
  Stack:    React Native, Next.js, Docker
```

**`projects`**
1. **Prisma/SQL → Chen ERD Generator** — Maps database schemas (Prisma / raw SQL) into Chen-notation ERDs automatically.
2. **React Native Expo App** — Cross-platform mobile app built with Expo and React Native.
3. **Dockerized Auto-Judging System** — Automated code evaluation system for competitive programming; supports multiple languages.

**`skills`**
* Frontend: Next.js · React · React Native · Expo · Tailwind CSS
* Backend: Node.js · PHP · Laravel · REST · WebSocket
* AI / ML: Gemini API · LangChain · Prompt Engineering
* DevOps: Docker · GitHub Actions · Linux · Nginx
* Databases: PostgreSQL · MySQL · Prisma ORM · Redis
* Tools: Git · VSCode · Postman · Figma

**`contact`**
* GitHub: https://github.com/fajryariansyah
* LinkedIn: https://linkedin.com/in/fajryariansyah
* Email: fajry@example.com

---

## 4. Deliverables

Provide the complete project structure and code files:

```
my-portfolio/
├── app/
│   ├── page.tsx           # root page, renders <Terminal />
│   └── globals.css        # custom scrollbar, body background
├── components/
│   └── Terminal.tsx       # all terminal logic & UI
├── tailwind.config.ts
├── package.json
└── next.config.ts
```

Tech stack: **Next.js 14 (App Router) + TypeScript + Tailwind CSS**.