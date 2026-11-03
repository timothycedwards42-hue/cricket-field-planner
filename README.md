# Cricket Field Tactics Builder & Match Planner

An interactive, browser-based cricket fielding and tactics planner designed for coaches, captains, and junior representative teams. It provides real-time field restriction auditing, junior safety compliance, dynamic player tagging, and high-resolution graphic export without requiring any app installations or backend servers.

---

## Key Features

### 1. Dynamic Pitch Geometry & Batter Orientation
* **RHB / LHB Mirroring:** Instantly flips the entire ground geometry (slips, point, cover vs mid-wicket, square leg) based on whether a Right-Hand Batter or Left-Hand Batter is on strike.
* **North / South End Striking:** Switch the bowling end between North (top) and South (bottom) with automated repositioning of bowlers and keepers.
* **Intelligent Auto-Naming:** Automatically labels every placed fielder based on authentic fielding terminology (e.g., *1st Slip, Gully, Deep Third, Sweeper Cover, Cow Corner, Short Mid-Wicket*).

### 2. Match Restrictions & Safety Auditing
* **Live Restriction Pill Badge:** Displays an active breakdown of fielders:
  * Deep (outside the 30-yard circle)
  * Inner Ring
  * Slips & Gully
  * Combined **Deep + Slips/Gully** metric for association-specific fielding quota rules.
* **10-Metre Junior Exclusion Zone:** A faint dashed arc in front of the active batter enforces junior safety regulations. If any close-in fielder (other than slips/keeper) is placed inside 10 metres, the live badge triggers an instant visual alert (`⚠ Safety: Fielder inside 10m arc!`).

### 3. Squad Roster & Positional Movement (Up to 14 Players)
* **Custom Names & Colours:** Customize up to 14 squad members with individual names and distinct colour swatches.
* **Multi-Position Tracking:** Place the same player multiple times across the field to demonstrate positional shifts (e.g., initial ring position moving to boundary defense for the death overs).
* **One-Click Role Auto-Placement:**
  * **[WK] Wicketkeeper:** Places the keeper at a realistic depth behind the striker's stumps.
  * **[B] Bowler:** Positions the bowler at the non-striker's delivery crease.
* **Drag-and-Drop Adjustment:** Drag any dot across the turf to fine-tune depth or angle; the position name updates in real time.

### 4. Custom Tactical Scenarios & Export
* **Scenario Manager:** Save, name, and recall custom tactical setups (e.g., *"Powerplay RHB"*, *"Death Overs Trap"*, *"Spinner Attacking"*) directly in your browser using local storage.
* **Match-Day Team Sheet Export:** Download a crisp PNG image that bundles both the field diagram and a neat 14-player team sheet legend formatted for printing, match-day folders, or parent messaging groups.

---

## How to Use

1. **Set Up the Context:** Enter your diagram title and select the striker's stance (RHB/LHB) and bowling end.
2. **Assign the Core Roles:** Click **[WK]** and **[B]** next to your keeper and bowler in the right squad panel to seat them automatically.
3. **Place Your Fielders:** Select a player from the squad roster and click anywhere on the oval to drop them into position.
4. **Demonstrate Movement:** Select the same player again and click their secondary position. Use the **Draw Move Arrow** tool to link their starting and ending spots.
5. **Add Tactical Notes:** Switch to **Add Tactical Text** to place field instructions (e.g., *"Save the single"*, *"Boundary rider"*).
6. **Save & Export:** Save the setup to your **Custom Scenarios** dropdown, or click **Export PNG Image** for a clean graphic with the squad roster legend attached.

---

## Technical Details

* **Single-File Architecture:** Pure HTML5 Canvas, Vanilla CSS, and JavaScript. Zero dependencies or build steps.
* **Client-Side Storage:** Uses browser `localStorage` to retain custom scenarios across sessions.
* **Feedback Integration:** Connected to Formspree for direct email submission of user ideas and bug reports.

