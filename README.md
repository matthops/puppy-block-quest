# Puppy Block Quest

A math platformer designed by two brothers. An orange puppy runs, jumps, and solves math problems to get home through four worlds: Block Meadow, Lava Land, Under the Sea, and Space Station.

- **Team mode:** One puppy, players take turns answering.
- **Race mode:** Two puppies side by side, first one home wins.
- **Math levels:** Add & Subtract (1st grade) or Multiply & Divide (3rd grade), picked per player.

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
