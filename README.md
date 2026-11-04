# Cricket Field Diagram & Tactics Planner

An interactive web application designed for cricket coaches, captains, and team managers to plan fielding setups, bowling strategies, and team scenarios. Built with vanilla HTML5 Canvas, modern JavaScript, and real-time Supabase cloud synchronization.

---

## Quick Start & Core Workflows

### 1. Setting Up the Match Context
* **Striker Stance:** In the left sidebar under **Striker Stance**, toggle between **RHB** (Right-Hand Batter) and **LHB** (Left-Hand Batter). The field position names, slip cordon side, and pitch lateral channels will adapt automatically.
* **Bowling End:** Toggle between **North End** (Top) and **South End** (Bottom) depending on which end of the pitch your bowler is running in from.
* **Overlays:** Use the toggle switches in the left panel to turn on/off:
  * **Player Names:** Displays player name badges next to each dot.
  * **Position Labels:** Displays formal fielding position terminology (e.g., *Cover*, *Deep Square Leg*).
  * **Pitch Lengths & Lines:** Overlays length bands and off/stump/leg channels onto the center pitch.
  * **Show Scoring Gaps:** Visualizes open boundary channels and real-time defensive shadows cast by fielders.
  * **10m Safety Arc:** Displays the junior safety exclusion zone in front of the striker's popping crease.

---

### 2. Managing the Squad (14 Players)
* **Select Active Player:** Click or tap any player card in the right **Squad Roster** sidebar to make them active (highlighted with an emerald halo).
* **Assign Roles (WK / Bowler):**
  * Tap **WK** on any player card to automatically set their position behind the stumps as the Wicketkeeper.
  * Tap **B** to assign and place them at the bowling crease.
* **Custom Names & Colors:** 
  * Click directly into a player's name field to edit their name inline.
  * Click the circular color swatch to choose a custom jersey color for that player.
* **Bulk Paste Squad:** Tap **📝 Paste List** at the top of the roster panel to paste player names from an email, team chat, or spreadsheet (comma-separated or one per line).
* **Save/Load Squad Lists:** Use the dropdown in the roster header to save named squads (e.g., *"Saturday XI"*, *"U13 Reps"*) or delete old lists.

---

### 3. Setting the Field
Use the floating **Tool Dock** situated directly above the oval:

* **● Fielder Tool (Default):**
  * **Place:** Select a player from the squad list, ensure `● Fielder` is active, then tap anywhere on the green turf.
  * **Move / Reposition:** Click and drag (or touch and drag) any placed fielder dot across the oval.
  * **Boundary Guard:** Fielder dots cannot be dropped or dragged outside the white boundary rope.
  * **Jersey Numbers:** Each dot clearly displays the player's roster number (`1`–`14`) directly inside the circle.
* **➔ Arrow Tool:**
  * Tap the start position (e.g., a fielder's starting mark), then tap the destination to draw a movement/cutting-off vector.
* **T Text Tool:**
  * Tap `T Text`, then tap anywhere on the field. A prompt will appear where you can enter tactical instructions (e.g., *"Save the Single"*, *"Catching Slip"*, *"Boundary Rider"*).
* **⌫ Delete Tool:**
  * Tap `⌫ Delete`, then tap any fielder dot, arrow, or text badge on the ground to remove it.
* **↶ Undo & ↺ Clear:**
  * Tap `↶ Undo` to step back your last action.
  * Tap `↺ Clear` to wipe all markings and reset field marks.

---

### 4. Reading the Tactical HUD & Scoring Zones
* **Field Quota Badge (Top-Right HUD):**
  * Audits field restrictions in real time: tracks total fielders, counts in the **Deep**, counts in the **Ring**, and numbers in the **Slips/Gully cordon**.
  * **Safety Alert:** If any fielder is positioned inside the 10m safety arc in front of the popping crease, the badge flashes red with a safety warning.
* **Dynamic Scoring Gaps (`Show Scoring Gaps`):**
  * **Golden Corridors:** Open batting lanes clear to the fence are highlighted in a soft golden-amber glow.
  * **Fielder Shadows:** Every placed fielder intercepts shots within their diving reach ($20\text{px}$) and casts a defensive shadow from behind their stance all the way to the boundary rope, clearly showing unprotected pockets.

---

### 5. 🎯 Pitch View & Bowling Target Pop-Out
Click **🎯 Pitch View** in the top navigation bar to open the dedicated 22-yard pitch pop-out modal:

* **Place Bowling Target:** Tap or click anywhere on the pitch to set the intended ball impact target.
* **Real-Time Analysis:** The callout box analyzes the impact point and reports tactical feedback (e.g., *"Good Length • 4th Stump Corridor"* or *"Yorker / Full • Straight (Stumps)"*).
* **Delivery Angle Toggle:**
  * **Over the Wicket:** Bowler releases from the left of the non-striker stumps (from the bowler's view).
  * **Around the Wicket:** Bowler releases from the right of the non-striker stumps.
* **Trajectory Arc:** Renders an animated delivery trajectory from the bowler's hand straight into the pitch target and through to the stumps.
* Tap **Save & Return to Field** to reflect the target and delivery line directly on the main ground diagram.

---

### 6. Scenarios, Sharing & Match-Day Mode
* **Scenario Ribbon (Bottom Bar):**
  * Save different tactical scenarios (e.g., *"Powerplay"*, *"Spin Attack"*, *"Death Overs"*) using the **+ Save** button.
  * Switch between match scenarios with a single tap on the horizontal scenario chips.
* **📺 Zen Mode (Presentation):**
  * Tap **📺 Zen Mode** (or press the `F` or `Esc` key on your keyboard) to collapse all sidebars and toolbars, maximizing the field canvas for huddles and tablet presentations.
  * Tap the floating **✕ Exit Zen** button (or press `Esc`) to restore normal controls.
* **🔗 Shareable Link:**
  * Tap **🔗 Share** in the top bar to copy a standalone URL containing the entire field setup, roster, and bowling target encoded into the link.
* **⬇ Export PNG:**
  * Tap **⬇ Export PNG** to download a high-resolution graphic combining the cricket ground diagram with a 14-player team sheet card.
* **Cloud Sync (Supabase):**
  * Tap the **Sync: Off** pill in the top header and enter your team code (e.g., `U13REPS`). All saved scenarios, rosters, and field setups will instantly synchronize across all devices using that code.
