# Releasing buzz-bingo-mobile-downloads

This repo is public. Nothing secret ever goes here.

1. Work on a branch. Stage named files only.
2. Open a pull request to `main`. Wait for green CI if any runs. Merge.
3. Keep the asset name `buzz-bingo-android-arm64.apk`. The only public Android link is `https://www.buzzbingo.app/tester-guide/`.

## Safety lock (git hook)
The file `.githooks/pre-push` refuses a direct push to a protected branch (main) on this Mac. It is a seat belt, not a wall: it only works in a clone where it is switched on, and a merge on GitHub itself is not checked.
- Switch it on once per clone: `git config core.hooksPath .githooks`
- Check it is on: `git config core.hooksPath` must print `.githooks`.
- Git worktrees of this repo share that setting.
- If a push is blocked, push a feature branch and open a pull request. Do not use `--no-verify`. Only Jana may override it, in the current chat.
