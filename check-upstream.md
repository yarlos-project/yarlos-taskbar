# Check Upstream Status

This guide helps you check if your YarlOS Taskbar repository is up to date with the original upstream source.

## Current Remote Configuration

First, check your current git remotes:

```bash
git remote -v
```

Expected output:

```
origin  https://github.com/yarlos-project/yarlos-taskbar.git (fetch)
origin  https://github.com/yarlos-project/yarlos-taskbar.git (push)
upstream        https://gitlab.com/AndrewZaech/aztaskbar.git (fetch)
upstream        https://gitlab.com/AndrewZaech/aztaskbar.git (push)
```

## If Upstream Remote is Missing

If you don't see the `upstream` remote, add it:

```bash
git remote add upstream https://gitlab.com/AndrewZaech/aztaskbar.git
git fetch upstream
```

## Check for Upstream Updates

### 1. Fetch latest changes from upstream (safe, doesn't change your code)

```bash
git fetch upstream
```

### 2. Check if there are any new commits in upstream/main

```bash
git log --oneline upstream/main --since="1 week ago"
```

### 3. Compare your main branch with upstream/main

```bash
git diff --stat main upstream/main
```

### 4. Check if tree hashes are the same (identical file content)

```bash
git rev-parse main^{tree}
git rev-parse upstream/main^{tree}
```

If these two hashes are the same, your files are identical to upstream.

### 5. See what files are different (if any)

```bash
git diff --name-only main upstream/main
```

### 6. Quick status check (combine fetch + compare)

```bash
git fetch upstream && git rev-parse main^{tree} upstream/main^{tree} | uniq | wc -l
```

- If output is `1`: trees are identical (up to date)
- If output is `2`: trees are different (updates available)

### 7. See upstream commit history without affecting your branch

```bash
git log --oneline --decorate upstream/main -10
```

## Summary

Run `git fetch upstream` first, then use the comparison commands above. These commands will show you what's changed upstream without modifying your local repository.

If you want to actually update your repository with upstream changes, you would then use:

- `git merge upstream/main` (brings full history, adds all contributors)
- Or cherry-pick specific commits to maintain clean contributor history

## Notes

- Your current `main` branch has clean history with only `yarlos-project` as contributor
- `upstream/main` contains the full history with all original contributors
- File content may be identical even with different commit histories</content>
  <parameter name="filePath">/Users/suthan/yarlos/yarlos-taskbar/check-upstream.md
