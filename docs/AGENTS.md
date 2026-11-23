# Instructions for coding agents

This directory is the source of a SaturnDocs site. SaturnDocs builds and publishes the site from Git: a push to the connected repository starts a build.

## Layout

- `docs.json`: site settings and navigation.
- `pages/`: one `.md` or `.mdx` file per page. Each page needs a `title` in its frontmatter.
- `public/`: images and other files, served from the site root.
- `openapi/`: OpenAPI specifications.

Any other file in this directory stops the publish. This file and `CLAUDE.md` are the exceptions: SaturnDocs accepts them and never publishes them.

## Before every commit

Run both checks from this directory and fix every error they report. Each error names a file, a line, a rule, and a fix.

```sh
npx saturndocs validate . --json
npx saturndocs lint . --json
```
