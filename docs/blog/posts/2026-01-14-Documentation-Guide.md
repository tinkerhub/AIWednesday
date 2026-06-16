---
title: "How to Document an AI Wednesday Session"
date: 2026-01-10
authors: [sebin]
description: >
  Guide on how to document an AI Wednesday journal entry.
---

*By [Sebin Thomas](https://tinkerhub.org/@sebin) · January 10, 2026*

AI Wednesday is a weekly, community driven gathering at TinkerSpace where people connect, share, and build.

From 2026 onwards, every session should have a short journal entry, usually written by the host.

# Why we document AI Wednesday

AI Wednesday is a weekly community gathering, but the conversations, demos, and learnings should not end when the session ends.

By documenting each AI Wednesday, we:

- Keep a clear log of what was discussed and built
- Help members who could not attend stay updated
- Make it easy for new members to understand the community’s direction
- Create a shared reference for ideas, projects, and follow ups
- Build a long term archive of our community journey

These short journal entries are not meant to be detailed reports. They are lightweight snapshots of each session, written so that any community member can quickly read, catch up, and continue the conversation.

## Documentation steps

1. Set up MkDocs Material on your computer
2. Run the site locally
3. Add a new journal post using the template
4. List the post in the site navigation
5. Push changes and raise a pull request

---

### Setup on your computer

First, you need setup the computer to run the `mkdocs` locally.

#### Prerequisites

- Install Python and pip - follow the guide [here](https://www.python.org/downloads/)
- Install MkDocs - follow the guide [here](https://squidfunk.github.io/mkdocs-material/getting-started/).
- Install Git - follow the guide [here](https://git-scm.com/install/)

---

### Fork, clone, and run locally

1. Fork the repository

- Open the upstream repository: [tinkerhub/AIWednesday](https://github.com/tinkerhub/AIWednesday)
- Click Fork (creates your copy under your GitHub account)

2. Clone your fork

```
git clone https://github.com/tinkerhub/AIWednesday.git
cd AIWednesday
```

3. Start the local dev server

Run this from the folder that contains `mkdocs.yml`:

```
mkdocs serve
```

MkDocs will serve the site locally (usually on `http://127.0.0.1:8000/`)

---

### Create a new AI Wednesday journal entry

Each session is a Markdown post that is listed in the site's left-hand **Journal** navigation, ordered by date. The navigation order, the session number, and the author byline are all maintained by hand, so follow every step below.

1. Create a new branch

```
git checkout -b add-AIWednesday-journal-YYYY-MM-DD
```

2. Add a new post file

Follow the existing pattern in the repository for where posts live.

- `docs/blog/posts/YYYY-MM-DD-title.md`

3. Add front matter

Add metadata for your post. The session number (`XX` in the title) is the **next number in date order** — look at the latest post in `docs/blog/posts/` and add one.

```
---
title: 'AI Wednesday XX : Name for the AI Wednesday'
date: YYYY-MM-DD
authors: [author]
description: >
  A Small Description
---
```

4. Add an author and date byline

The site does not render an author header automatically, so add a byline as the first line under the front matter. It links to your TinkerHub profile and is what readers see as the credit:

```
*By [Author Full Name](https://tinkerhub.org/@your-handle) · Month DD, YYYY*
```

5. List the post in the navigation

Open `mkdocs.yml` and add your post to the `Journal` section under `nav`, in date order (newest at the bottom):

```
nav:
  - index.md
  - Journal:
    - blog/index.md
    # ... existing posts ...
    - blog/posts/YYYY-MM-DD-title.md
```

If you skip this step, the post will not show up in the left navigation.

6. Add yourself to the authors list (first-time contributors)

If this is your first time contributing, add your details to `docs/blog/.authors.yml` so the author record stays complete:

```
  author-username:
    name: Author Full Name
    description: Author tag line
    avatar: https://avatars.githubusercontent.com/u/xxxxxxxx
    url: Tinkerhub App profile URL
```

In the avatar section, replace the `xxxxxxx` with your GitHub profile id.

---

### Journal template (copy paste)

Use this template inside your post:

```
---
title: 'AI Wednesday XX : Name for the AI Wednesday'
date: YYYY-MM-DD
authors: [author]
description: >
  A Small Description
---

*By [Author Full Name](https://tinkerhub.org/@your-handle) · Month DD, YYYY*

## Overview
Write 3 to 6 lines on what happened this week. Mention the theme and the general vibe.

## Topics
- Topic 1
- Topic 2
- Topic 3

## Project Presentation
- Name – project title (one line summary if needed)
- Name – project title

## Photos
### Group photo
![Group photo](../assets/images/YYYY-MM-DD/group-photo.png)

### Activity photo
![Activity photo](../assets/images/YYYY-MM-DD/activity-photo.png)

## Highlights
- One key takeaway (learning, decision, win, or community moment)

## Next Week
- Topic: TBD
- Host: TBD

```

#### Notes for photos:

- Store images in `docs/blog/assets/images/YYYY-MM-DD/` (create the folder for your session date).
- Reference them with a relative path like `../assets/images/YYYY-MM-DD/group-photo.png`.
- Keep filenames simple and consistent.
- Always add meaningful alt text.

---

### Preview your changes

While mkdocs serve is running, open the local site and check:

- The post appears in the **Journal** list in the left sidebar, in the correct date order.
- The author and date byline shows under the title.
- Images load.
- Headings look correct and spacing is clean.

---

### Commit, push, and open a pull request

1. Commit and push to your fork

```
git add .
git commit -m "Add AI Wednesday journal for YYYY-MM-DD"
git push -u origin add-AIWednesday-journal-YYYY-MM-DD
```

2. Create a pull request to upstream

On GitHub, open your fork and you should see a prompt to create a PR. GitHub’s flow for PRs from forks is documented here

PR checklist:

- Title includes the date and session name.
- Session number follows date order.
- Post is listed in `mkdocs.yml` under Journal.
- Author and date byline added.
- Post follows the minimum structure.
- Photos included or clearly marked pending.
- Previewed locally.

---

Suggested style (keep it consistent)

- Prefer short paragraphs and bullet lists.
- Avoid long intros.
- Name people and projects clearly (credit matters).
- If something is TBD, write “TBD” instead of leaving it blank.

---
