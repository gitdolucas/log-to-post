# Log-to-Post

Log what you built (text, images, commits, branches); get LinkedIn, X, Reddit, and standup copy in one go.

A Cursor skill that keeps a structured daily log and turns it into platform-ready drafts so you can build in public without rewriting the same thing four times.

## What it does

- **Log** — One file per day (`logs/YYYY-MM-DD.md`) with typed entries: what you started, shipped, discovered, what blocked you, what you’re learning.
- **Post** — From that log, generate drafts for LinkedIn, X (Twitter), Reddit, and a standup summary. Output goes to `posts/YYYY-MM-DD.md` (or separate files per platform if you prefer).

One source of truth; multiple formats.

## Quick start

1. **Install** the skill in Cursor (or use this repo as your base path).
2. **Choose a base path** for logs and posts when prompted (e.g. this repo, or `~/dev-log`). The skill creates `logs/` and `posts/` there and remembers the path via `.log-to-post`.
3. **Log** by saying things like:
   - *"Log: Shipped the auth refactor and merged to main."*
   - *"Log my day"* and paste or describe what you did.
   - Or ask to log from git commits, images, or chat.
4. **Generate posts** by asking:
   - *"Turn my log into posts"*
   - *"Post ideas from my logs"*
   - *"Standup from my logs"*

You can scope by date (e.g. today + last 2 days) or by entry type (e.g. only `shipped` + `discovered`).

## Folder structure

```
<base-path>/
  .log-to-post          # Marks base path (optional)
  logs/
    YYYY-MM-DD.md       # One log file per day
  posts/
    YYYY-MM-DD.md       # Generated drafts (all formats in one file by default)
  references/
    log-format.md       # Log entry format and types
    prompts-and-platforms.md  # Content style per platform
```

## Log entry types

| Type       | Use for                          |
| ---------- | -------------------------------- |
| `started`  | Began something new              |
| `running`  | In progress                      |
| `blocked`  | Stuck or waiting                 |
| `discovered` | Learned or found something    |
| `shipped`  | Delivered or merged              |
| `learning` | Studying or practicing           |

Entry format (frontmatter + content) and optional fields (`project`, `branch`, `repo`, `links`, `tags`) are described in [references/log-format.md](references/log-format.md).

## Generating drafts

- The skill reads your chosen log file(s), aggregates the content, and applies the style rules in [references/prompts-and-platforms.md](references/prompts-and-platforms.md) for each platform.
- Default: one file per day `posts/YYYY-MM-DD.md` with sections for X, LinkedIn, Reddit, Standup (and optionally Discord changelog).
- You can ask for separate files per platform: `posts/YYYY-MM-DD-linkedin.md`, `posts/YYYY-MM-DD-twitter.md`, etc.

Edit the generated drafts as needed before posting.

## References

- **[references/log-format.md](references/log-format.md)** — Log entry structure, types, and optional metadata.
- **[references/prompts-and-platforms.md](references/prompts-and-platforms.md)** — Content philosophy and platform-specific rules for LinkedIn, X, Reddit, and Standup.

## Skill definition

The behavior and checklists for the Cursor agent are in [SKILL.md](skills/log-to-post/SKILL.md). Use the `skills/log-to-post/` folder when installing or extending the skill in Cursor.
