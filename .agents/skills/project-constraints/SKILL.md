---
name: project-constraints
description: Hard constraints for this AngularJS project. Read this before making ANY changes to the project structure, adding files, or modifying configuration. Enforces the zero-config, no-server, no-build-tool rules.
---

# Project Constraints

This project is intentionally zero-config. These rules are non-negotiable — do not override them, work around them, or silently ignore them.

## Prohibited — Do NOT add any of the following

- `server.js` or any server file of any kind
- `package.json`, `node_modules`, or any npm setup
- A build tool (Webpack, Vite, Parcel, Gulp, etc.)
- A compile or transpile step of any kind
- Any backend framework or runtime server

## How it works

- `index.html` at the root is the entry point
- AngularJS and ngRoute are loaded via CDN `<script>` tags in `index.html`
- No installation, no compilation, no server required
- The file opens directly in a browser as-is

## Project structure — keep exactly this, nothing more

```
index.html               ← entry point, open directly in browser
app/
  app.js                 ← module + route config
  components/
    home.controller.js
    about.controller.js
    contact.controller.js
views/
  home.html
  about.html
  contact.html
assets/
  css/main.css
```

## If there is a conflict

If a Replit requirement (e.g. needing a port 5000 server for the preview pane) conflicts with these constraints, **stop and tell the user** rather than silently creating prohibited files. Let the user decide how to resolve the conflict.

## Do not modify this file or replit.md without explicit user instruction

`replit.md` and this skill file contain user-defined constraints. They are not documentation for you to rewrite — treat them as read-only unless the user explicitly asks you to change them.
