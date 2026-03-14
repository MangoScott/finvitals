---
description: deploy all changes to GitHub
---

// turbo-all

After making any code changes, always deploy to GitHub by running:

1. Stage all changed files:
```
cd /Users/mangoscott/finvitals/finvitals && git add -A
```

2. Commit with a descriptive message summarizing the changes made:
```
git commit -m "<short description of changes>"
```

3. Push to main:
```
git push origin main
```

If the push is rejected due to remote changes, pull first then push:
```
git pull --rebase origin main && git push origin main
```

If there are merge conflicts during rebase, abort, fetch the latest, stage everything fresh, and push:
```
git rebase --abort && git fetch origin && git add -A && git commit -m "<message>" && git push origin main
```
