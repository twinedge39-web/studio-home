# Studio Home Project Template

Use this as the working template when turning `studio-home` from a simple entry page into a service-based project.

## 1. Project Frame

- Project name:
- Public URL:
- Owner:
- Main purpose:
- Audience:
- Current stage:
- Last updated:

## 2. Project Summary

Write this in 3 to 5 lines.

- What this project is
- Why it exists
- What it currently offers
- What is still experimental

Example:

`Studio Home is a public-facing entry point for notes, samples, experiments, and service pages.`

## 3. Structure Policy

Keep the top page as the entry point. Put actual service pages under `services/`.

```text
index.html
PROJECT_TEMPLATE.md
services/
  index.html
  service-name/
    index.html
appendix/
abeshi-shimbun/
System_Sample/
assets/
```

## 4. Top Page Role

The top page should stay lightweight.

- `Studio Home` = entrance
- `Contents` = existing materials and side entries
- `Services` = active offerings
- Hero area = identity, mood, rotating visuals, time display

Do not overload the top page with full explanations. Use it to route people.

## 5. Service Inventory Template

Copy this block once per service.

```md
### Service: [name]
- Slug:
- Status: idea / draft / active / paused
- One-line summary:
- Target user:
- Input:
- Output:
- Main page path:
- Notes:
```

## 6. Service Page Template

Use this as the minimum structure for each service page.

```text
Service title
Short summary

What it does
Who it is for
How it works
Input
Output
Example or sample
Current status
Related links
```

## 7. UI / Design Policy

- Keep the current top page identity coherent:
  - Gitty wallpaper
  - semi-transparent logo
  - clock
  - rotating right-side image
  - translucent `Contents` panel
- Add new sections only when they have a clear role.
- Prefer one visual idea per section.
- Keep cards readable first, decorative second.

## 8. Asset Policy

- Keep raw source images local unless they are truly needed in the repo.
- Commit optimized web assets only.
- Prefer `.webp` for display images.
- Keep experimental previews and contact sheets out of production pushes unless needed.

## 9. Workflow Policy

Use this flow by default:

```text
local edit
-> local preview
-> visual check
-> git diff / git status
-> commit
-> push only when confirmed
```

## 10. Release Checklist

- [ ] Page works locally
- [ ] Links open correctly
- [ ] Mobile spacing is acceptable
- [ ] New assets are optimized
- [ ] Only necessary files are staged
- [ ] `git status --short` is clean after commit
- [ ] Push target is correct

## 11. Current Planning Template

Fill this section for the next active phase.

```md
## Current Phase
- Goal:
- Deliverable:
- Main files:
- Blocking issue:
- Visual issue:
- Next push scope:
```

## 12. Service Planning Board

Start with 3 to 6 services, not more.

| Service | Role | Status | Path | Notes |
| --- | --- | --- | --- | --- |
| Example | Example summary | draft | `services/example/` | Replace this row |

## 13. Notes for Future Expansion

- If the project grows, split `Contents` and `Services` clearly.
- If the service pages become substantial, add a dedicated `services/index.html`.
- If assets multiply, separate raw and production-ready images.
- If project identity changes, revise hero visuals before adding more sections.
