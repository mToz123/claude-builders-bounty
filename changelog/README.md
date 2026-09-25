# Changelog skill

Build CHANGELOG.md from commits after the latest git tag. Prefixes map to Added, Fixed, Changed, and Removed. Commits with no known prefix go under Other. The tagged commit itself is not included.

## Run

```
bash changelog.sh /path/to/repo
```

The script writes CHANGELOG.md in that repo and prints the git range it used.

## Setup

1. Put changelog.sh somewhere on disk and run chmod +x changelog.sh.
2. From any git repo that has at least one commit, run bash changelog.sh.
3. Open CHANGELOG.md in that repo. If a tag exists, only commits after it are listed.
