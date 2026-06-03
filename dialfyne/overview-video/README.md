# Dialfyne — Overview Launch Video

A ~39s, 1080p premium SaaS launch explainer built with Hyperframes.

**Scenes:** hook (62% unanswered) → cost (97% never call back) → brand reveal →
Voice AI → AI Roleplay → proof numbers → CTA.

Brand + type spec lives in `design.md`. Source of truth is `index.html`.

## Develop / check / render

```bash
npm run dev      # live preview server
npm run check    # lint + validate + inspect
npm run render   # render to MP4
```

## Rendering inside the Claude-on-the-web sandbox

This managed environment blocks the public gsap CDN host and ships no `ffmpeg` on PATH,
so two one-time setup steps are needed before `render` works here. (Neither is needed in a
normal local environment with internet + ffmpeg installed.)

```bash
# 1. Vendor gsap locally (index.html references ./gsap.min.js; it is git-ignored)
cp ../../node_modules/.bun/gsap@*/node_modules/gsap/dist/gsap.min.js ./gsap.min.js

# 2. Put the bundled ffmpeg-static binary on PATH
ln -sf "$(ls ../../node_modules/.bun/ffmpeg-static@*/node_modules/ffmpeg-static/ffmpeg)" /usr/local/bin/ffmpeg
```

If you take this composition to a normal environment, swap the `<script src="gsap.min.js">`
tag in `index.html` back to the CDN (`https://cdn.jsdelivr.net/npm/gsap@3.14.2/dist/gsap.min.js`).
