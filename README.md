# repos

Pin your repositories and see their status at a glance.

```
$ repos
  REPO                         BRANCH                                   DIRTY      PUSH
  ----------------------------  ---------------------------------------- ---------- --------------------
  case-management-pipeline     feature/two-col-transfer                 ● 2 modified   ↑ 1 to push
  personal-site                main                                     ✓ clean        ✓ synced
  brk                          main                                     ✓ clean        ✓ synced
```

Shows for each pinned repo:
- Current branch (or detached HEAD)
- Working directory status (staged, modified, untracked files)
- Push/pull status vs upstream (commits ahead or behind)

## Install

```bash
# Clone and symlink
git clone https://github.com/alexlazarian/repos.git ~/.repos
ln -s ~/.repos/repos /usr/local/bin/repos

# Or just download
curl -o /usr/local/bin/repos https://raw.githubusercontent.com/alexlazarian/repos/main/repos
chmod +x /usr/local/bin/repos
```

## Usage

```bash
repos                   # show status of all pinned repos
repos pin               # pin the current directory
repos pin ~/Dev/myapp   # pin a specific repo
repos unpin             # unpin the current directory
repos list              # list pinned repo paths
```

## Config

Pins are stored at `~/.config/repos/pins` (one path per line). Override the location with:

```bash
export REPOS_PINS="$HOME/.repos-pins"
```

## Dependencies

- **git** (required)

## License

MIT
