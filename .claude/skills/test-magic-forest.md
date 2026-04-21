Open magic-forest-counting.html in the browser, then print and walk through this manual test checklist:

```
start "C:\Users\vijit\Desktop\aitest\magic-forest-counting.html"
```

Then output the following checklist for the user to verify in the browser:

---

## Magic Forest Counting — Manual Test Checklist

**Initial render**
- [ ] Sky-to-meadow gradient background visible
- [ ] Tree with canopy, trunk, and branch rendered
- [ ] Owl visible in the tree hollow with blinking animation
- [ ] Exactly **3 red apples** on the branch at startup
- [ ] Exactly **3 filled dots** (red) and 2 empty dots (grey) in counter bar
- [ ] Blue `+` button (stick cross) on bottom-left
- [ ] Yellow `-` button (leaf) on bottom-right

**Adding apples (tap `+`)**
- [ ] Apple bounces in with squash-stretch animation
- [ ] Owl does a happy bounce after each press
- [ ] Counter dot fills red for each apple added
- [ ] At **5 apples**: owl performs full dance animation
- [ ] At **5 apples**: `+` button dims to ~40% opacity and stops responding

**Removing apples (tap `-`)**
- [ ] Apple falls and fades out
- [ ] Owl shrugs/frowns after each press
- [ ] Counter dot turns grey for each apple removed
- [ ] At **0 apples**: owl shows sad face
- [ ] At **0 apples**: `-` button dims to ~40% opacity and stops responding

**Resize / scaling**
- [ ] Resize the browser window — scene scales proportionally
- [ ] No horizontal scrollbar or overflow at any window size
- [ ] Scene stays centered vertically and horizontally

---

Report any failures back and I'll fix them.
