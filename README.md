# Blog

A personal blog.

**Status: not yet implemented.** This repository holds the design and the
intended behaviour. The code is not written yet.

## What it is

A place to write, kept deliberately simple.

Posts are Markdown files in a folder. The site is built from them and nothing
else. There is no database, no admin panel, and no account. Writing a post
means writing a file, and publishing it means committing it.

The simplicity is the point. A blog that needs a running server to show an
old post is a blog you will stop writing in.

## Writing a post

A post is a Markdown file with a little frontmatter:

```yaml
---
title: "On keeping a commonplace book"
date: 2026-03-14
tags: [writing, notes]
draft: false
---
```

The body is ordinary Markdown. A `<!-- more -->` marker, or simply the
`excerpt` field, decides where the preview on the index ends and the post
begins.

**`draft: true`** keeps a post out of the published site without moving the
file anywhere. It stays in the folder, it stays in version control, and it
does not appear until you flip the flag.

## How it is organised

**The index.** Every published post, newest first, with its title, date,
tags, and the first paragraph or so.

**Tags.** Posts are filed by tag, and each tag gets a page listing what is
filed under it.

**Archive.** Posts grouped by year, because that is how you look for
something you wrote a while ago.

**The post itself.** The full text, with a link back to the index and to the
posts either side of it.

## Why plain files

**It works without the blog.** The posts are Markdown. If this project is
abandoned, the writing is still there, in a form that any editor can open
and any other tool can read.

**It fits how you already work.** A post is a file in a folder, next to
everything else you write. Committing it is the same gesture as committing
anything else.

**It cannot lock you in.** There is no format proprietary to this project.
The only thing it adds is a build step that turns Markdown into HTML, and
that output is disposable.

## What it would be written in

TypeScript, with a static build. The site is generated ahead of time and
served as files, so there is nothing to keep running.

## Licence

MIT.
