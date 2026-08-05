# TamaPoke

## Git workflow

Work directly on `main`. Do not create feature branches, and do not open pull
requests unless explicitly asked.

Write commit messages in English. The upstream history and the in-code comments
are in Spanish — do not match them.

Remotes:

- `fork` — `git@github.com:danielberndt/TamaPoke.git` — ours, push here
- `origin` — `https://github.com/socquique/TamaPoke.git` — upstream, never push

## Parallel agents

Several agents may be working on `main` at the same time, so the working tree
is shared and will contain edits you did not make.

- Stage explicitly: `git add <path>` for the files you actually touched. Never
  `git add -A`, `git add .`, or `git commit -a` — they sweep up other agents'
  in-progress work.
- Run `git status` before committing and confirm every staged path is yours.
- Leave unrelated modified files alone. Do not revert, stash, or "clean up"
  changes you cannot account for.
- A file that changed since you last read it may have been edited by another
  agent, not by the user. Re-read before editing rather than assuming.
