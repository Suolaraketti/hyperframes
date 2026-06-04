# Dialfyne — Logo Sting

~8.5s, 1080p standalone logo animation (intro/outro). The symbol draws itself stroke by
stroke, the three prongs extend into the three pillars (AI Voice, AI Roleplay, AI Automations),
then it resolves into the full Dialfyne lockup.

Built from the official symbol paths (`assets/`), animated with GSAP `stroke-dashoffset`
draw-on. Brand + type spec in `design.md`.

## Develop / check / render

```bash
npm run dev      # live preview
npm run check    # lint + validate + inspect
npm run render   # render to MP4
```

## Sandbox render setup (Claude-on-the-web only)

The web sandbox blocks the gsap CDN and ships no ffmpeg on PATH. One-time:

```bash
cp ../../node_modules/.bun/gsap@*/node_modules/gsap/dist/gsap.min.js ./gsap.min.js
ln -sf "$(ls ../../node_modules/.bun/ffmpeg-static@*/node_modules/ffmpeg-static/ffmpeg)" /usr/local/bin/ffmpeg
```

Outside the sandbox, swap `<script src="gsap.min.js">` back to the gsap CDN.
