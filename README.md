# TZPPlus

<img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/tzp_vanilla.gif" width="360"> <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/tzp_eladshud.gif" width="360">

*Left: the vanilla HUD. Right: with EladsHUD+.*

Makes the **TZP Inhalant** worth carrying. Inhale it to `heal`, see exactly how much `gas` is left, and build up `damage reduction` that also protects you from fall damage. Push it too far and you may take a `Lethal Dose`.

Fully configurable. Gameplay settings are synced from the host, so everyone plays with the same numbers.

---

## Features

<details>
<summary>🩹 Healing</summary>

- Heals `5 HP per second` while inhaling (up to 100 HP).
- Stops bleeding / limping once you are back above `10 HP`.
- Your teammates see your new health without the "got hurt" flinch.

</details>

<details>
<summary>🔋 Gas meter</summary>

- The TZP's remaining gas shows in the `battery meter` while you hold it.
- A full tank lasts `38 seconds` of inhaling (configurable, see 🧪 TZP item).
- The TZP is never treated as a battery item, so it can't be "charged" at the ship's charger.

</details>

<details>
<summary>🧪 TZP item</summary>

- Set how long one TZP lasts: `Seconds of gas per TZP` (vanilla `38 seconds`). The battery meter and the seconds left follow it.
- Set the TZP-Inhalant's `store price` (vanilla `$120`). Store sales still apply.
- Both are synced from the host, so everyone has the same tank and pays the same price.

</details>

<details>
<summary>🛡️ Damage reduction</summary>

- Inhaling builds up damage reduction: `+2% per second`, up to `40%`
  - `20%` after 10 seconds, `40%` after 20 seconds.
- Reduces **all damage**, including `fall damage` (can be turned off).
  - Example: a 100 damage fall becomes `80` at 20% and `60` at 40%.
- The buff holds while you inhale and for `10 seconds` after you stop, then fades by `2% per second`.
- **Exploit protection:** with no buff, inhaling counts right away. Once you have a buff, a new puff must last `2.5 seconds` before it stacks again and refreshes the timer. Shorter puffs add nothing.
- Instant kills (e.g. being grabbed by a Forest Giant) are not affected.

</details>

<details>
<summary>☠️ Lethal Dose & Withdrawal</summary>

*Optional, off by default.*

- Inhale TZP for `20 seconds` in one high (short puffs add up until the TZP has fully worn off) and you take a **Lethal Dose**.
- **Lethal Dose:** you're concussed (`motion blur`, `red tint` and `dark edges`) until every TZP effect has worn off. Only the game view gets it, so your HUD stays readable.
- **Withdrawal:** right after the Lethal Dose ends, for `60 seconds`:
  - you walk and run `15% slower`
  - you jump `15% lower`
  - stamina refills `15% slower` and drains `8% faster`
  - being alone makes you paranoid `1.5x faster`
- Inhaling TZP during Withdrawal makes it wear off `10x faster` (every 0.1 s of inhaling takes 1 s off).
- With **[FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/)**, its Sedatives make Withdrawal wear off `2x faster` while they last.

</details>

<details>
<summary>🧠 Paranoia</summary>

- TZP calms you down: while you inhale, your paranoia (the game's insanity, which brings the creepy sounds and moving doors) drops `2 per second`.
- Withdrawal does the opposite: alone, your paranoia rises `1.5x faster`.
- With **[FrailtyPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyPlus/)** you can see it: its `Paranoid` debuff shows up at 75%.

</details>

<details>
<summary>🦴 Frailty injuries</summary>

*Optional, off by default. Needs [Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/).*

- While you inhale TZP, broken / fractured `legs` and `arms` heal `10x faster`.

</details>

<details>
<summary>🎨 UI Display</summary>

- <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_damage_reduction.png" width="32"> `Damage Reduction` (buff): builds up while you inhale: you take less damage (fall damage too). The value above it is the %.
- <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_withdrawal.png" width="32"> `Withdrawal` (debuff): after a Lethal Dose, you're slower, jump lower, your stamina refills slower and drains faster, and being alone makes you paranoid faster.
- <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_lethal_dose.png" width="32"> `Lethal Dose` (debuff): too much TZP: you're concussed (blur, red tint, dark edges) until every TZP effect has worn off.

&nbsp;&nbsp;
<details>
<summary>Icon</summary>

- Every effect gets an icon with its `value` or `time left`.
- Placed in the bottom-left corner next to the vanilla HUD, right after Frailty's injury icons (same size and tilt), with the value above each icon.
- Move it or resize it with `Icon row X offset`, `Icon row Y offset` and `Icon row size`.

</details>

<details>
<summary>Text</summary>

- Small lines in the bottom-right corner instead of icons, one line per effect (e.g. `Damage Reduction 24%`, `Withdrawal 41s`).
- Move it or resize it with `Text X offset`, `Text Y offset` and `Text size`.

</details>

**Additional UI features**

- We also added icons for the **vanilla TZP buff / debuff** the game never shows you (*off by default*, turn on `Show vanilla TZP effects`):
  - <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_tzp_rush.png" width="32"> `TZP Rush` (buff): you move faster and sprinting barely uses stamina.
  - <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_slippery.png" width="32"> `Slippery`: slow to start and stop, you slide around.
  - <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_dizzy.png" width="32"> `Dizzy`: your camera lags behind your mouse.
  - <img src="https://raw.githubusercontent.com/SleepyMiles/TZPPlus/main/images/icon_warped.png" width="32"> `Warped`: pitched-up voice, hazy vision, muffled sound.
- Timers show how long until the effect wears off if you stop now (they count up while you keep inhaling).
- **Color changes:**
  - The vanilla stamina meter fades to `gold` while the damage reduction is active.
  - It turns `red` while you have Withdrawal.
- You decide what shows up: the effect display can be set to `Icons`, `Text` or `Off`, and TZPPlus's own effects (`Damage Reduction`, `Lethal Dose`, `Withdrawal`) and the vanilla TZP effects can each be turned **on or off** on their own.

</details>

---

## Configuration

Every number is adjustable in `BepInEx/config/Miles.TZPPlus.cfg`, or in-game with **LethalConfig**.

| Section | What | Synced? |
|---|---|---|
| 1. Healing | on/off, HP per second | ✅ from the host |
| 2. Damage Reduction | on/off, include fall damage, max damage reduction %, reduction gained per second %, minimum puff seconds, grace seconds, decay % per second | ✅ from the host |
| 3. Display UI | gas meter, effect display (icons / text / off), show TZPPlus effects, show vanilla TZP effects (off by default), buff icon numbers in buff color, icon row position / size, text position / size, stamina meter gold / red, color | ❌ client side only |
| 4. Lethal Dose | on/off (off by default), seconds of inhaling, withdrawal seconds, withdrawal strength %, withdrawal stamina drain %, withdrawal countdown while inhaling | ✅ from the host |
| 5. Frailty injuries | on/off (off by default), leg / arm injury countdown while inhaling | ✅ from the host |
| 6. EladsHUD compatibility | health / stamina bar gold, red stamina bar during withdrawal | ❌ client side only |
| 7. TZP item | seconds of gas per TZP, store price | ✅ from the host |
| 8. Paranoia | withdrawal paranoia multiplier, TZP calm per second, Sedatives Withdrawal speed | ✅ from the host |

---

## Compatibility

- **Everyone in the lobby needs this mod.**
- **Elad's HUD / [EladsHUD+](https://thunderstore.io/c/lethal-company/p/SleepyMiles/EladsHUDPlus/)**
  - The gas meter also shows the `seconds of gas left`.
  - The health and stamina bars fade to `gold` while the damage reduction is active (stronger buff = stronger color), and the health bar stays visible while buffed. Low stamina still turns the bar red.
  - The stamina bar turns `red` during Withdrawal.
  - With the **SleepyMiles fork** of Elad's HUD, the icons go in its row under the health bar, with tooltips when you point at them.
- **[Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/) / [FrailtyPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyPlus/)**: optional, for faster-healing leg / arm injuries. The icons sit right after Frailty's own icons. FrailtyPlus' injuries also come from the damage after TZPPlus' reduction, so the buff lowers them too. With FrailtyMedical installed, TZP can't heal you while you're bleeding (FrailtyPlus' rule).
- **[FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/)**: its Antibiotics clear Withdrawal and its Sedatives make it wear off faster; its icons sit on the same row.
- **[Drinkable](https://thunderstore.io/c/lethal-company/p/SleepyMiles/Drinkable/)**: its icons sit on the same row.
- **LethalConfig**: change every setting in-game.
- **AdvancedCompany**: stacks with the `Protective Skin` perk (multiplicatively, e.g. 10% + 20% = 28%).
- ⚠️ **Do not use together with** EnhancedTZP, TZPReworkedHealing or TZPHealingCustom. They also change the TZP and would heal on top of this mod.

## Play them together

These mods are made by **SleepyMiles** to work as one set. They share one row of buff / debuff icons (or EladsHUD+'s status row) and one **CONSUMABLES** store section, and they know about each other's effects. Each one also works on its own (FrailtyMedical needs FrailtyPlus).

| Mod | What it adds |
|---|---|
| **TZPPlus** (this mod) | The TZP heals you, shows its gas, builds up damage reduction (fall damage too). Too much gives a Lethal Dose. |
| [FrailtyPlus](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyPlus/) | Injuries: broken / fractured legs and arms, bleeding, concussions, Paralyze. A rebuilt Frailty. |
| [FrailtyMedical](https://thunderstore.io/c/lethal-company/p/SleepyMiles/FrailtyMedical/) | *Beta.* Bandage, First Aid Kit, Morphine (revive a teammate), Epinephrine, Painkillers and Antibiotics to treat them. |
| [Drinkable](https://thunderstore.io/c/lethal-company/p/SleepyMiles/Drinkable/) | Drink the Red soda, 19 new drinks with their own buffs, the Soda Machine and the Drink Machine. |
| [EladsHUD+](https://thunderstore.io/c/lethal-company/p/SleepyMiles/EladsHUDPlus/) | Elad's HUD for V81, with a status row that shows every buff, debuff and injury from all of these with the `time left`. |

---

## Download & bug reports

- Get it from [Thunderstore](https://thunderstore.io/c/lethal-company/p/SleepyMiles/TZPPlus/) with your mod manager, or download the zip from [GitHub Releases](https://github.com/SleepyMiles/TZPPlus/releases).
- Found a bug or have an idea? [Open an issue](https://github.com/SleepyMiles/TZPPlus/issues/new/choose) and attach your `BepInEx/LogOutput.log`.

---

## Credits

- [Frailty](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Frailty/) by IntegrityChaos for the icon style and the concussion effect.
- Inspired by [EnhancedTZP](https://thunderstore.io/c/lethal-company/p/Asc3nt/EnhancedTZP/) (Asc3nt), [TZPReworkedHealing](https://thunderstore.io/c/lethal-company/p/Hotoni/TZPReworkedHealing/) (Hotoni) and [TZPHealingCustom](https://thunderstore.io/c/lethal-company/p/riverbible/TZPHealingCustom/) (riverbible).
- The code is written from scratch for game version V.81.
