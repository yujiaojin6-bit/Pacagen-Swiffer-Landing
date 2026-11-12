# PUSH BRIEF v2 — push only, do not rebuild, do not generate images

The landing page v2 is ALREADY BUILT and on disk in this folder. Do NOT rebuild it, do NOT generate any images or GIFs, do NOT edit index.html content. The user will supply all remaining photos/GIF herself later; image slots are intentional placeholders (dashed boxes labelled 待补充).

Files already here (verify with `ls` first): index.html (v2, ~25 KB), README.md, assets/pack-main.png (the real MAX pack image she supplied — used in hero + buy box), assets/hero.webp, lifestyle.webp, cloths.webp, pain.gif (v1 generated images — NOT referenced by v2 index.html anymore, leave them alone), plus assigb_ppt.pdf and Pacagen_Interview_Assignment.pdf for reference. The 4 assets-v2 images from the earlier brief are NOT used and must NOT be added.

## Your one job
1. Open this folder in VS Code: /Users/beibeijin/Desktop/Pacagen-Swiffer-Landing (NOT the portfolio folder -profolio).
2. Verify index.html references only assets/pack-main.png (no hero.webp / pain.gif). Preview it locally and check: pack image shows in hero + buy box, 4 dashed placeholder boxes show (pain GIF, before/after, how-it-works, lifestyle), cost calculator slider works, Old vs MAX toggle works, FAQ opens, sticky buy bar appears on scroll.
3. In the VS Code terminal, in this folder: `git init` (if no .git yet), `git add .`, commit "MOP & GO MAX landing page v2 — placeholders, user pack image", create a NEW public GitHub repo `yujiaojin6-bit/pacagen-swiffer-landing` (use `gh repo create` if available, otherwise create it on github.com in the browser and add the remote), push to main.
4. Enable GitHub Pages from main branch, root. Wait ~1-2 min, then verify the live page loads at https://yujiaojin6-bit.github.io/pacagen-swiffer-landing/ — pack image visible, placeholders visible, calculator works. Hard refresh if needed.
5. If the repo name is taken, use `pacagen-swiffer-landing-2026` and report the actual URL. NEVER push to the portfolio repo `-profolio`.
6. You are responsible for every Allow/approval in your own VS Code session. Do not leave VS Code until the live page is verified.

## Report back
GitHub repo URL, live Pages URL, commit hash, and confirmation of what you verified live (pack image, placeholders, calculator, toggle). If an approval card times out or the Mac goes offline, stop and report exactly where — do not loop retries on your own.
