# Puppy Block Quest

A math platformer designed by two brothers. An orange puppy runs, jumps, and solves math problems to get home through twenty-one worlds: Block Meadow, Lava Land, Under the Sea, Space Station, Candy Land, Snowy Peaks (slippery ice), Jungle (bouncy mushrooms), Desert (tumbleweeds), Cloud Kingdom (bouncy clouds), Dragon Castle (moving platforms), and Rainbow Land (rainbow slides, star bridges, color blocks, and three bosses, designed by Ben and Luke), Robot Factory (conveyor belts), Pirate Bay (floating rafts), Toy Store (trampolines), Dino Valley (geysers), New York City (window-washer lifts), Bee Garden (sticky honey), Dungeon (darkness and crumbly bridges), Kitty Kingdom (yarn balls and cushions), and Water Park (slides, inner tubes, water jets, and swimmable pools), and Fun Park (roller coaster carts and parade paths). A 🎲 Surprise Me button picks a random world.

- **Team mode:** One puppy, players take turns answering.
- **Race mode:** Two puppies side by side, first one home wins.
- **Math levels:** Add & Subtract (1st grade) or Multiply & Divide (3rd grade), picked per player.
- **Word problems per player:** Each player can pick 📖 Word problems (Off, or 1–5 stars) from a dropdown next to their math level, so story problems show up in any world.
- **Adaptive math + mastery tracking:** Each track is an 8-rung skill ladder (Add & Subtract: add within 5 → two-digit ± with regrouping; Multiply & Divide: ×2/×5/×10 → 3-digit ± and 2-digit × 1-digit). A rung is mastered at 8 of the last 10 right on the first try with median answer time under the rung's goal; the game then levels up automatically. Under 50% first-try accuracy over the last 6 steps back one rung. Problem mix: ~70% current rung, 20% review, 10% preview; missed facts recur until answered right. Word problems can be set to Auto to follow the ladder.
- **📊 Grown-ups page:** Press and hold for 3 seconds to open. Per player: totals, first-try accuracy, average speed, problems per day, a mastery bar per rung, trouble facts, level-change history, and overrides (set rung, lock, reset). Data is per device.
- **Coin Shop:** Each player keeps their own coins between rounds and buys skins, swords, and power-ups. Paying means solving the subtraction for the change.
- **Paint Studio:** Buy paint colors (including Gold and Rainbow) and paint designs on your puppy or cat.
- **Lucky blocks:** Bonk a ❓ block and answer right for coins or a free power-up for that round.
- **Level Maker:** A map editor. Pick a piece, tap the map to place it, drag to scroll, make the level as long as you want, erase, and save to My levels. Saved levels also show in a ⭐ My Levels section on the main menu for one-tap play. Saved levels live in the browser on each device.
- **Bosses ON/OFF:** A menu switch (off by default). With bosses off, each boss becomes a wall, so the math stays.
- **Music:** Original chiptune tune for each world. Toggle it with the 🎵 button.

Coins and purchases are saved in the browser on each device, keyed by player name. Typing the same name brings back the same wallet.

## Put it on GitHub Pages

**Option A: in the browser**

1. Create a new **public** repo on your personal account, e.g. `puppy-block-quest`.
2. Click **Add file → Upload files** and drag in everything in this folder.
3. Go to **Settings → Pages**. Under "Build and deployment," pick **Deploy from a branch**, then `main` and `/ (root)`. Save.
4. About a minute later the game is live at `https://<your-username>.github.io/puppy-block-quest/`.

**Option B: from the terminal**

```bash
cd puppy-block-quest
git init && git add . && git commit -m "Puppy Block Quest"
gh repo create puppy-block-quest --public --source=. --push
gh api -X POST repos/{owner}/puppy-block-quest/pages -f "source[branch]=main" -f "source[path]=/"
```

Check that `gh auth status` shows your personal account before you run `gh repo create`, not your work account.

## Install it on the iPad

1. Open the game link in **Safari**.
2. Tap **Share → Add to Home Screen**.
3. Launch it from the home screen. It opens full-screen and works offline after the first load.

Play in landscape. In race mode, each kid gets one side of the screen.

## Play with Switch controllers

1. Hold the small sync button on a Joy-Con (or the Pro Controller) until the lights run.
2. On the iPad, go to **Settings → Bluetooth** and tap the controller.
3. Open the game. A "Controller is ready" message appears.

- **Move:** stick or D-pad. **Jump:** any face button.
- **Answering:** move left and right to highlight an answer, then press a face button.
- **Start / +:** starts the game or goes to the next world.
- **Race mode:** the first controller is Player 1 and the second is Player 2.

Single Joy-Cons held sideways haven't been tested. If one acts strange, try a Pro Controller or a pair of Joy-Cons.

## Keyboard (Mac)

- **Team:** arrows or W A D to move and jump, 1–4 to answer.
- **Race:** Player 1 uses A D W and 1 2 3 4. Player 2 uses the arrow keys and 7 8 9 0.

## Updating

Edit `index.html` and push. The page checks for a new version each time it opens online. If you change the icons or `manifest.json`, bump `CACHE` at the top of `sw.js` so installed copies refresh.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole game |
| `manifest.json` | App name, icon, full-screen and landscape settings |
| `sw.js` | Offline support |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Home Screen icons |
