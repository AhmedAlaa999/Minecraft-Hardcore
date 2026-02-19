# ⛏ Minecraft Survival Simulator

```
 ███████╗██╗   ██╗██████╗ ██╗   ██╗██╗██╗   ██╗ █████╗ ██╗
 ██╔════╝██║   ██║██╔══██╗██║   ██║██║██║   ██║██╔══██╗██║
 ███████╗██║   ██║██████╔╝██║   ██║██║██║   ██║███████║██║
 ╚════██║██║   ██║██╔══██╗╚██╗ ██╔╝██║╚██╗ ██╔╝██╔══██║██║
 ███████║╚██████╔╝██║  ██║ ╚████╔╝ ██║ ╚████╔╝ ██║  ██║███████╗
 ╚══════╝ ╚═════╝ ╚═╝  ╚═╝  ╚═══╝  ╚═╝  ╚═══╝  ╚═╝  ╚═╝╚══════╝
                    // HARDCORE MODE //
```

> A pixel-art browser survival game built in pure HTML, CSS & JavaScript. No frameworks. No dependencies. Just blocks, mobs, and death.

🔗 **[▶ Play it Live](https://ahmedalaa999.github.io/Minecraft-Hardcore/)** &nbsp;|&nbsp; 👤 **Made by [Ahmed Alaa](https://github.com/ahmedalaa999)**

---

## 📸 Overview

A dark, gritty browser-based survival simulator inspired by Minecraft. Mine resources, fight mobs, manage your hunger and health, level up — and try not to let a Creeper end your run.

Built with a **pixel-art aesthetic**: chunky bars, hard drop shadows, Press Start 2P typography, and a full death screen that doesn't pull punches.

---

## 🎮 Features

| Feature | Description |
|---|---|
| ❤️ **Health System** | Take damage from mobs and Creepers. Reach 0 and it's game over. |
| 🍖 **Hunger Mechanic** | Actions drain hunger. Let it hit zero and you're toast. |
| ⭐ **XP & Leveling** | Earn XP from mining and combat. Level up as XP thresholds increase. |
| 🌙 **Night Mode** | Toggle night — mob damage gets buffed, atmosphere goes dark. |
| 💣 **Creeper Events** | Trigger a Creeper explosion for a punishing -30 (or -40 at night) HP hit. |
| 🎒 **Inventory** | Collect random loot from mining: wood, stone, diamonds, and more. |
| 💀 **Death Screen** | Full-screen death overlay with respawn. All progress lost. |
| 🔴 **Damage Flash** | Red screen flash on every hit for visceral feedback. |

---

## 🕹️ How to Play

**1. Stay alive.**  
Your health drops when mobs hit you or Creepers explode. Hunger drains from actions.

**2. Mine for loot.**  
Hit `⛏ Mine` to dig and find random resources. Costs 10 hunger, earns 15 XP.

**3. Eat when hungry.**  
`🍖 Eat Food` restores 30 hunger. Don't let it bottom out.

**4. Fight to level up.**  
`🗡 Fight Mob` deals random damage (0–20 HP) but rewards 20 XP. Risk vs reward.

**5. Avoid Creepers.**  
`💣 Creeper!` hits for 30 HP — 40 HP at night. Only press it if you're feeling brave.

**6. Survive the night.**  
Toggle `🌙 Night` to increase the difficulty. All mob damage gets a bonus.

---

## 📊 Game Mechanics

### Health
- Starts at `100`
- Damaged by mob fights and Creeper explosions
- Does **not** regenerate automatically
- Reaching `0` triggers the death screen

### Hunger
- Starts at `100`
- Drained by: Mining (`-10`), Fighting (`-15`), Creeper (none)
- Restored by eating (`+30`, capped at 100)

### XP & Levels
- Mining: `+15 XP`
- Fighting: `+20 XP`
- Level up threshold: `100 × current level`
- XP resets to 0 on level up (excess carries over)

### Night Mode
- Mob fight damage: `+8 bonus`
- Creeper damage: `30 → 40 HP`
- Visual: full blue-dark overlay on screen

---

## 🗂️ File Structure

```
minecraft-survival/
│
├── index.html        ← Everything. The whole game. 261 lines.
└── README.md         ← You're reading this.
```

No build step. No bundler. No `npm install`. Open the file and play.

---

## 🚀 Getting Started

```bash
# Clone or download
git clone https://github.com/yourname/minecraft-survival-sim

# Open in browser
open index.html
```

Or just drag `index.html` into any browser window. Done.

---

## 🎨 Design System

The UI is built around a deliberate **pixel-art dark theme**:

- **Fonts**: `Press Start 2P` (headers/labels) + `VT323` (body/log) — both from Google Fonts
- **Color palette**:
  - Background: `#0d0d0d` / `#1a1a1a`
  - Health bar: `#FF3333`
  - Hunger bar: `#FF9900`
  - XP bar: `#7FFF00`
  - Accent/grass: `#5D9B3F`
- **Pixel grid**: CSS background-image overlay at 16×16px
- **Shadows**: Hard `box-shadow: 4px 4px 0 #000` — no blur, pixel-perfect
- **Transitions**: `steps()` easing on bars for chunky pixel animation

---

## ⚙️ Technical Details

- **Pure HTML/CSS/JS** — zero external scripts beyond Google Fonts
- **No localStorage** — session only, by design (permadeath is a feature)
- **~261 lines** total
- **CSS custom properties** for the full color system
- **Overlay layers** managed via z-index stacking (night, damage flash, death screen)
- All state held in plain JS variables: `health`, `hunger`, `xp`, `level`, `inventory[]`

---

## 🔮 Potential Additions

- [ ] Crafting system (combine inventory items)
- [ ] Multiple mob types with different damage profiles
- [ ] Hunger passive drain over time
- [ ] Health regen when hunger is high
- [ ] Save/load via `localStorage`
- [ ] Sound effects using the Web Audio API
- [ ] Day/night cycle timer (auto-toggles)
- [ ] Biome system affecting loot tables

---

## 📄 License

MIT — do whatever you want with it. Build on it, break it, ship it.

---

## 👤 Author

**Ahmed Alaa**
- 🌐 [Live Demo](https://ahmedalaa999.github.io/Minecraft-Hardcore/)
- 🐙 [GitHub](https://github.com/ahmedalaa999)

---

```
> Waiting for input...
```

*Made by **Ahmed Alaa** with ⛏ and zero regrets.*
