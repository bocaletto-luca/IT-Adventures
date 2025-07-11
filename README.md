# IT Adventures – Nerdstown Chronicles  
#### Author: Luca Bocaletto  

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge&logo=gnu)](LICENSE) [![Language: Python](https://img.shields.io/badge/Language-Python-blue?style=for-the-badge&logo=python)](https://www.python.org/) [![Linux-Compatible](https://img.shields.io/badge/Linux-Compatible-blue?style=for-the-badge&logo=linux)](https://www.kernel.org/) [![Status: Complete](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)](https://github.com/bocaletto-luca/Directory-Monitor)

**A comedic, tech-heavy text adventure in pure open-source style**  

In **IT Adventures**, you don the hoodie of Luca, a quick-witted sysadmin with a knack for command-line humor. Your playground is **Nerdstown**, a neon lit city where Ethernet cables crisscross sidewalks like vines, and cafés brew “Espresso at 5 GHz.” You’ll start in your cluttered hacker den—monitor towers balanced like Jenga blocks, Linux stickers plastering every surface, and a cat furiously tapping on a keyboard—before venturing out to:

- **TechCorp’s open-space**: dodge crashing 500 errors, scavenge discarded hard drives, and face your first fetch quest.  
- The **Bean Overclock Café**: where baristas challenge you with impromptu Linux quizzes while you sip a “Latte 16-Thread.”  
- The **Data Center**: a labyrinth of buzzing server racks where you’ll wield soldering irons and power banks to revive dead disks.  
- Hidden corners like the **Retro Museum**, where you prove your vintage lore with Apple I trivia, and the **Secret AI Lab**, locked behind sudo-only doors.

Along the way you’ll tackle:

  • **Linux quizzes** on commands, file permissions, TCP ports and shell scripts—each correct answer awards XP and reputation.  
  • **Hardware repair missions**: swap bad RAM, solder broken traces, and replace failed power supplies to unlock new areas.  
  • **Fetch quests** to locate rare items (RGB RAM sticks, Raspberry Pi modules, power banks) scattered across Nerdstown.  
  • **Dynamic events**—random DDoS alerts, surprise blackouts, retro‐tech puzzles—that force you to think on your feet and type lightning-fast fixes.  
  • **Eccentric NPCs**: from an RGB-obsessed memory vendor to “Diego The Skid,” a forty-year hacker legend who tests your scp skills.

Every success nets you **XP**, in-game **credits**, open-source **tokens** and coveted **reputation**. Level up to earn `sudo` privileges, open restricted rooms and negotiate high-stakes side-quests. Whether you’re debugging a cron job gone rogue, outsmarting a firewall with clever iptables rules, or simply showing off your grep mastery, **IT Adventures** turns every shell command into a triumph—one witty one-liner at a time.

<p align="center">
  <a href="./index.html">
    <img src="https://img.shields.io/badge/View–English%20Site–index.html-blue?style=for-the-badge" alt="English Version" />
  </a>
  <a href="./index-ita.html">
    <img src="https://img.shields.io/badge/Visualizza–Versione%20Italiana–index-ita.html-blue?style=for-the-badge" alt="Versione Italiana" />
  </a>
</p>

---

## 📁 Project Structure

```
it-adventures/
├── data/                # Game content (editable)
│   ├── world.json       # Rooms, descriptions, exits, events
│   ├── missions.json    # Missions list (quiz, fetch, event)
│   ├── items.json       # Items, descriptions, usable contexts
│   └── npcs.json        # NPCs, dialogues, side-quests
│
├── save.json            # Auto-save state
│
├── src/                 
│   ├── data.py          # Load/save data, game state
│   ├── ui.py            # Colorful rendering with Rich (HUD, rooms, tables)
│   ├── engine.py        # Main menu and game loop
│   ├── quests.py        # Mission logic (quiz, fetch, events)
│   └── npcs.py          # NPC dialogues and interactions
│
├── requirements.txt     # Dependencies (rich)  
├── Dockerfile           # Minimal container  
├── .gitignore           
└── README.md            # This file  
```

---

## 🚀 Installation & Launch

1. **Clone the repository**  
   ```bash
   git clone https://github.com/bocaletto-luca/IT-Adventures.git
   cd IT-Adventures
   ```

2. **Create a virtual environment (recommended)**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Start the game**  
   ```bash
   python3 src/engine.py
   ```

5. **Using Docker**  
   ```bash
   docker build -t it-adventures .
   docker run -it it-adventures
   ```

---

## 🎮 Main Commands

### Main Menu  
- `1` New Game  
- `2` Load Game  
- `3` Save Game  
- `4` Help  
- `5` Exit  

### In-Game  
- `go <direction>` (e.g. `go north`)  
- `take <item>` (e.g. `take kit_soldering`)  
- `use <item>` (when supported)  
- `inventory` / `inv`  
- `missions`  
- `start <id>` (start a mission)  
- `talk <npc_id>` (interact with NPC)  
- `status` (show HUD)  
- `look`  
- `save`  
- `exit` (return to menu or quit)

---

## 🌟 Key Features

- **Comic & Technical**: witty lines about Linux, sysadmin life, open-source culture, “sudo”, “root”, “bugs”, “RGB RAM.”  
- **Branching Missions**: Linux quizzes, fetch quests, sysadmin puzzles.  
- **NPC Side-Quests**: humorous dialogues, reputation gains, collectible badges.  
- **Dynamic HUD**: levels, XP, credits, OSS tokens and reputation always visible.  
- **Modular Design**: add rooms, missions, NPCs or items simply by editing the JSON files in `data/`.

---

## 🔧 How to Extend

- **Add New Rooms**  
  Edit `data/world.json` to define titles, descriptions, exits, items and optional events.

- **Create Missions**  
  Expand `data/missions.json` with types `quiz`, `fetch` or `event`, specifying prompts, options and rewards.

- **Define NPCs**  
  Add dialogues and side-quests in `data/npcs.json`, complete with intros, dialogue trees and rewards.

- **Customize the HUD**  
  Tweak `src/ui.py` to change colors, layout or ASCII art.

---

## 📜 License

Distributed under **GNU GPL v3**. See `LICENSE` for details.

---

Thank you for choosing **IT Adventures**! Get ready to laugh, learn, and celebrate the power of open source in an unparalleled text-based journey. Have fun!  

---
