# 🚀 Profile Setup Guide

Follow these steps to make your GitHub profile look great.

## 1. Create the special repo
Create a **public** repository named exactly the same as your username:
`rajaramsharma/rajaramsharma`

(GitHub shows a README from this repo at the top of your profile page.)

## 2. Add the files to the repo ROOT
Place these in the root of the repo:
- `README.md`
- `avatar_animated.gif`   (your spinning circular avatar)
- `.github/workflows/snake.yml`   (keep the folder structure)

Final structure:
```
rajaramsharma/
├── README.md
├── avatar_animated.gif
└── .github/
    └── workflows/
        └── snake.yml
```

## 3. Commit & push to main
```bash
git add .
git commit -m "✨ Add profile README, animated avatar, and snake action"
git push origin main
```

## 4. Turn on the snake animation
- Go to the repo → **Actions** tab → enable workflows if prompted.
- Open **Generate Snake Animation** → click **Run workflow**.
- It creates an `output` branch with `github-snake-dark.svg`.
- After it finishes once, the snake graphic in your README will appear.
  (It then auto-updates every 12 hours.)

## 5. Done ✅
Refresh your profile page: https://github.com/rajaramsharma

---

### Tips
- All stats/streak/trophy cards fill in automatically using your real username.
- Want the avatar ring in a different color or spin speed? Just ask.
- If an image is slow to load the first time, that's the third-party
  service waking up — refresh after a minute.
