# Astro Netlify Repro

GH Issue: https://github.com/withastro/astro/issues/7540

## Versions
Astro 3.5.0
Netlify 3.0.4

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