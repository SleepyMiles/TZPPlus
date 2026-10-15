# Changelog

## 1.1.0

<details>
<summary>✨ New</summary>

- **Buff / debuff icons** with their `value` or `time left` for `Damage Reduction`, `Lethal Dose`, `Withdrawal`, and the vanilla TZP effects `TZP Rush`, `Slippery`, `Dizzy` and `Overdose`.
  - Shown in the bottom-left corner next to the vanilla HUD (after Frailty's icons), or under the health bar with the SleepyMiles fork of Elad's HUD (with tooltips).
  - Or pick `Text` (bottom-right lines) or `Off`.
  - TZPPlus's own effects and the vanilla TZP effects can be turned on/off separately.
- **Lethal Dose** (optional, off by default): inhaling `20 seconds` in one high concusses you (`motion blur`, `red tint`, `dark edges`) until every TZP effect has worn off. Only the game view gets it, the HUD stays readable. Frailty is not needed.
- **Withdrawal** after a Lethal Dose: `60 seconds` of `15% slower` walking / running, `15% lower` jumps, `15% slower` stamina refill and `8% faster` stamina drain. Inhaling TZP makes it wear off `10x faster`.
- **Frailty injuries** (optional, off by default): with Frailty installed, inhaling TZP makes broken / fractured legs and arms heal `10x faster`.
- **Color changes:** the vanilla stamina meter fades to `gold` while the damage reduction is active and turns `red` during Withdrawal (Elad's HUD too).

</details>

<details>
<summary>🔧 Changes</summary>

- Damage reduction cap raised to `40%` (was 20%). It still builds at `2% per second` (20% after 10 s, 40% after 20 s).
- Damage reduction now holds for `10 seconds` (was 5) after a counted puff before it starts to fade.
- The "TZP -X% DMG" text is now the `Text` option of the new effect display.

</details>

<details>
<summary>⚙️ Settings</summary>

- New: `Max damage reduction %` and `Reduction gained per second %` (replace `Max reduction %` and `Seconds to max`).
- `Include fall damage` moved right under `Enable damage reduction`.
- `3. Display UI` (client side only): `Effect display`, `Show TZPPlus effects`, `Show vanilla TZP effects`, `Buff icon numbers in buff color`, icon row and text position / size, stamina meter gold / red.
- New sections `4. Lethal Dose` and `5. Frailty injuries` (synced from the host).
- New section `6. EladsHUD compatibility` (client side only) for the Elad's HUD bar colors.

</details>

## 1.0.2

<details>
<summary>Details</summary>

- Damage reduction: with no buff, inhaling now counts right away (no 2.5 s wait).
- With a buff already active, a new puff must last `2.5 seconds` before the buff stacks again; stacking starts from that moment and the grace timer resets. Shorter puffs still do nothing.

</details>

## 1.0.1

<details>
<summary>Details</summary>

- Fixed an error that stopped the mod from working.

</details>

## 1.0.0

<details>
<summary>Details</summary>

- Initial release for Lethal Company V.81.
- TZP heals while inhaling (`5 HP/s` by default), synced to other players without hurt animations.
- TZP gas shown in the battery meter (vanilla HUD and Elad's HUD, incl. seconds left).
- Damage reduction buff from inhaling: up to `20%`, builds up over 10 s, 2.5 s minimum puff, 5 s grace, 2%/s decay. Includes fall damage.
- "TZP -X% DMG" text, and Elad's HUD health / stamina bars fade to the buff color.
- All gameplay settings synced from the host (CSync); display settings per player; editable in-game with LethalConfig.

</details>
