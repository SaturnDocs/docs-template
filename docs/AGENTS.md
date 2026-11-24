# Instructions for coding agents

This directory is the source of a SaturnDocs site. SaturnDocs builds and publishes the site from Git: a push to the connected repository starts a build.

## Layout

- `docs.json`: site settings and navigation.
- `pages/`: one `.md` or `.mdx` file per page. Each page needs a `title` in its frontmatter.
- `public/`: images and other files, served from the site root.
- `openapi/`: OpenAPI specifications.

Any other file in this directory stops the publish. This file and `CLAUDE.md` are the exceptions: SaturnDocs accepts them and never publishes them.

## Before every commit

Run the check from this directory and fix every error it reports. Each finding names a file, a line where one exists, a rule, and a fix.

```sh
npx saturndocs check . --json
```

An error fails the publish or shows readers a broken page. A warning is a heuristic: compare it with the page, correct the page if the warning is right, and leave a correct page as it is.
