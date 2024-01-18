# Astro Netlify Repro: 404

GH Issue: https://github.com/regisphilibert/astro-netlify-404-repro

## Versions
Astro 4.2.1
Netlify 4.1.1

## Description
404 routes are not picked up by Netlify's 404 logic.

Expected: Netlify serves its default Neltify 404 page or theproject's own /404.html

🚫
```
src/
├─ pages/
│  ├─ [...page].astro (static works)
│  ├─ persons/[id].astro (ssr 404)
```
✅
```
src/
├─ pages/
│  ├─ [page].astro (static works)
│  ├─ persons/[id].astro (ssr works)
```

## Step to reproduce

1. Deploy to Netlify
2. From homepage, navigate to any `/ererer` route.