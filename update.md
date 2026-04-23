Act as an expert frontend developer specializing in React/Next.js and Tailwind CSS. I want to build a modern, purely frontend, terminal-themed personal portfolio website focusing on exceptional UI/UX.

Please generate the complete code based on these exact specifications:

### 1. Overall UI (macOS Terminal Illusion)
* **Background:** A subtly blurred, dark abstract wallpaper to give depth.
* **Terminal Window:** Center the terminal in a floating window container.
* **Window Header:** A macOS-style title bar at the top with three colored dots (red, yellow, green) on the left, and a title in the center: `fajry — -zsh — 80x24`. Include a soft drop shadow behind the window.
* **Terminal Body:** Dark background (`#1e1e1e`), customized thin scrollbar. Monospace font (e.g., Fira Code).

### 2. Core UX & Animations
* **Boot Sequence (Initial Load):** When the component mounts, simulate a rapid boot sequence using a fast typing effect before revealing the prompt. E.g., print `[ OK ] Booting portfolio OS...`, `[ OK ] Loading dependencies...`, then clear and show the initial prompt.
* **Tab Auto-completion:** If the user types a partial command (e.g., `pro`) and presses the `Tab` key, automatically complete it to the matching command (e.g., `projects`). Prevent default tabbing behavior.
* **Prompt Line:** `fajry@macbook:~$ ` (color-coded).
* **Auto-Focus & History:** Input must auto-focus. Pressing `Arrow Up`/`Arrow Down` cycles through previous command history. Auto-scroll to bottom on new output.

### 3. Frontend Commands to Implement
Implement a command parser for these specific commands:
* `help`: Lists available commands.
* `neofetch`: Outputs a classic terminal-style profile. Left side: a simple ASCII art logo. Right side: nicely aligned info (Role: Software Engineer, Shell: zsh, Location: Banda Aceh, Stack: React Native, Next.js, Docker).
* `projects`: Lists 3 featured projects (Prisma to Chen ERD Generator, React Native Expo App, Dockerized Auto-Judging System) with brief descriptions.
* `clear`: Clears the terminal screen.
* *Unknown Command:* Output `zsh: command not found: [command]`.

Please provide the Next.js component code (e.g., `Terminal.tsx`) combining state management for the history/input and Tailwind classes for the macOS window UI.