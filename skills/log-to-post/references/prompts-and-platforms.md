# Content philosophy and platform rules

Use this when generating post drafts from log content.

## Content philosophy

**Context:** This comes from a personal dev log: a raw, honest record of what the user is building, breaking, discovering, and delivering day to day with Claude and Cursor. Not a formal portfolio or tutorial channel.

- **Philosophy:** No thought leadership, no hot takes, no hustle-porn. Just: "Here's what I was building today, and what happened."
- The interesting content comes from real work: a weird edge case, a prompt that worked well, a feature that shipped in 20 minutes when it would have taken 3 hours before. That's the tone.
- **Goal:** Authentic build-in-public, sustainable sharing. The post should sound like someone actually building and sharing the journey, not selling or performing.

## Unique styles

Generate one draft per format. Each format has a **distinct style and length**—LinkedIn narrative, X punchy, Reddit show-and-ask, standup bullets. Do not mix styles; keep each output copy-paste-ready for its context.

## Platform rules

### LinkedIn

**[LinkedIn Agent]** Professional but real — as in the vision: "What did I learn, what does it mean for how we work?" Confident, conversational tone, light storytelling, short lines. Include 3–5 hashtags at the end (#FullStackDeveloper #ReactJS #NodeJS #AWS #RemoteWork). Encourage engagement (question or "What do you think?"). 150–300 words. Insight-driven: what was learned and what it means for how we work. Subtle emoji. Avoid sounding desperate or salesy.

### X / Twitter

**[X Poster Agent]** Punchy. One idea. Hook first — as in the vision. Casual and quick (ideal max 280 characters). Thread only if the topic deserves more space. Energetic emojis, 2–4 hashtags (#FullStack #WebDev #RemoteDeveloper #100DaysOfCode). Hook + link + subtle CTA. Dev-community style: technical and relatable.

### Reddit

**[Reddit Poster Agent]** Casual and honest. Dev-community voice — as in the vision: "No hype, just here's what I ran into." Humble, value-first (not salesy to avoid bans). Share as "showing what I built" or "asking for feedback". Respect r/webdev, r/forhire, r/SideProject. Catchy title, body with details and link, ask for feedback/roast. Start with "I built this..." or similar; end with "Thoughts?" or "Open to remote freelance if it fits". No excessive hashtags. **Output:** title in the first paragraph, blank line, then body.

### Standup

Factual, bullet-style. No hashtags or CTAs. Fixed structure:

- **Yesterday**: What was done or in progress. Map from log types `shipped`, `running`.
- **Today**: What you plan to do or are starting. Map from `started`, `learning`.
- **Blockers**: Anything stuck or waiting. Map from `blocked`.

One short bullet per item; keep the whole standup scannable in under a minute.

## Generating drafts

- Input: aggregated log text (and optional project name).
- Output: one draft per format (LinkedIn, X, Reddit, Standup). Each format uses a distinct style per this document. For Reddit, output only the post (title in first paragraph, then body). For Standup, output only the three sections (Yesterday / Today / Blockers) as bullets. No meta-commentary; only copy-paste-ready text.
- If the user has shared base portfolio/links (e.g. portfolio URL, "open to freelance"), weave that in naturally per platform; do not invent facts or links.
