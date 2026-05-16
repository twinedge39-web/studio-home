# Studio Home Thread Handoff

Use this file to resume the `studio-home` project in a new thread without re-explaining the whole context.

## 1. Project Status

- Project: `studio-home`
- Local repo: `E:\studio-home`
- Public repo: `https://github.com/twinedge39-web/studio-home`
- Current role: public-facing entry page, now moving toward service-based structure
- Current phase: top page design is largely settled; next step is project/service expansion

## 2. What Is Already Done

- `index.html` is the active top page
- Gitty wallpaper background is in place
- semi-transparent logo is in place
- live date/time display is in place
- right-side hero image rotates hourly
- `Contents` section styling has been heavily tuned already
- Gitty and NFT hero images are already prepared as web assets

## 3. Current Top Page Identity

Keep these as the baseline unless there is a clear reason to change them:

- Gitty repeating wallpaper
- dark blue overlay
- logo on the left
- rotating portrait image on the right
- clock above the logo
- translucent `Contents` panel

## 4. Main Files

- Top page: `E:\studio-home\index.html`
- Planning template: `E:\studio-home\PROJECT_TEMPLATE.md`
- Old markdown entry: `E:\studio-home\index.md`
- Assets folder: `E:\studio-home\assets`

## 5. Current Published Commits

Recent important commits:

- `18bbed2` `Refine contents panel styling`
- `b4230e5` `Refresh Gitty hero images`
- `2b3f7b8` `Add rotating studio hero images`
- `3c9ac74` `Add patterned background`
- `57a444c` `Add logo hero and mobile spacing`

## 6. Current Local-Only State

At handoff time:

- `PROJECT_TEMPLATE.md` exists locally and is untracked
- many raw / experiment / preview assets remain untracked on purpose
- do not push raw source images or preview sheets by accident

## 7. Push Policy

Default workflow:

```text
local edit
-> local preview
-> visual check
-> git diff / git status
-> commit
-> push only when explicitly decided
```

Important rule:

- push only the necessary production files
- leave raw, test, preview, and contact-sheet files local unless they are explicitly needed

## 8. Known Untracked Categories

These are mostly intentional and should not be blindly staged:

- raw Gitty sources
- raw NFT sources
- preview HTML files
- contact sheets
- intermediate transparent / staggered background experiments
- local JPG working files used before web conversion

## 9. Design Decisions Already Reached

- plain white cards felt too bright
- the darker glass-card direction fits better
- `Contents` should feel calmer and more integrated with the wallpaper
- the page works better as a “base / studio / hub” than a simple plain homepage
- the top page now feels distinct enough to support actual service content

## 10. Current Direction

The next structural step is to turn the site into a project with services.

Recommended direction:

- keep `index.html` as the entrance
- add `services/`
- create `services/index.html`
- create service-specific subpages under `services/`
- keep `Contents` for supporting materials and legacy links

## 11. Next Recommended Actions

Pick up from here:

1. Fill `PROJECT_TEMPLATE.md`
2. Decide the first 3 to 6 services
3. Add `services/`
4. Build `services/index.html`
5. Decide whether top-page cards should split into `Contents` and `Services`

## 12. Resume Prompt Template

Paste this into the next thread if needed:

```text
We are continuing the `studio-home` project in `E:\studio-home`.
Read `THREAD_HANDOFF.md` and `PROJECT_TEMPLATE.md` first.
Assume the top-page design is mostly settled.
Do not push raw or preview assets by accident.
Next task: [write the specific next task here].
```
