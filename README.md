# Al-Tawheed Content

Static content repository for the [Al-Tawheed](https://github.com/mdarif/Al-Tawheed) Flutter app.

Deployed via **Cloudflare Pages** at `https://al-tawheed-content.pages.dev`

## Structure

```
tawheed/
  catalog.json        ← lecture catalog (fetched by the app on launch)
  cover.jpg           ← book cover image
  audio/
    lec-001.mp3       ← 50 lectures, lec-001 through lec-050
    lec-002.mp3
    ...
    lec-050.mp3
_headers              ← Cloudflare Pages cache + CORS config
```

## Content

| | |
|---|---|
| Book | Sharah Kitab al-Tawheed (شرح كتاب التوحيد) |
| Speaker | Fazilat Shaikh Abdullah Nasir Rahmani |
| Language | Urdu |
| Lectures | 50 |
| Classes | 15 |
| Total duration | 27h 7m |
| Total size | ~390 MB |

## Cloudflare Pages Setup

- Build command: *(none)*
- Output directory: `/`
- Deployed URL: `https://al-tawheed-content.pages.dev`

## Updating the catalog

Edit `tawheed/catalog.json` and push to `main`. Cloudflare Pages redeploys automatically. The app picks up the new catalog within 1 hour (cache TTL).

Audio files use a 1-year immutable cache — never modify an existing file in place. The lecture series is complete; no new audio is expected.
