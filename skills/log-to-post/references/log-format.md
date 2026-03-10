# Log entry format

Use this structure for each entry in `logs/YYYY-MM-DD.md`.

## Entry types

- `started` — began something new
- `running` — in progress
- `blocked` — stuck or waiting
- `discovered` — learned or found something
- `shipped` — delivered or merged
- `learning` — studying or practicing

## Per-entry format (Markdown)

Use a clear block per entry. Option A (frontmatter-like) or Option B (headings) below.

### Option A (recommended)

```markdown
---
type: discovered
project: log-to-post
links: []
---

Fixed the generate route; TDD caught a missing validation. Will add one more test for edge case.
```

Example with git context (optional `branch` and `repo`):

```markdown
---
type: shipped
project: my-app
branch: main
repo: my-app
links: [https://github.com/me/my-app/commit/abc123]
---

Merged auth refactor; dashboard and export are live.
```

### Option B (plain headings)

```markdown
### discovered · log-to-post

Fixed the generate route; TDD caught a missing validation. Will add one more test for edge case.
```

- **type** (required): one of the entry types above.
- **content** (required): one or more paragraphs of plain text.
- **project** (optional): short project or context name.
- **branch** (optional): branch name when the entry comes from git.
- **repo** (optional): short repo name or path for context.
- **links** (optional): list of URLs (e.g. Claude chat, GitHub commit or repo).
- **tags** (optional): list of tags for filtering later.

When appending, add a horizontal rule between entries for readability:

```markdown
---
type: shipped
project: my-app
---

Released v1.2; dashboard and export are live.

---
type: learning
---

Reading the TDD skill; going to try strict red-green-refactor this week.
```
