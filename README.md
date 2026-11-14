# Velqira

**Search without the noise.**

A private, ad-free search engine in a single HTML file. No server. No account. No tracking.

## Why Velqira

- **Private:** your search history stays on your device.
- **Clean:** no ads, no clutter, light and dark mode.
- **Smart:** results from several open sources are merged, de-duplicated and ranked on your device.
- **Simple:** one file, no build step, no dependencies.

## Run it

1. Download `velqira.html`.
2. Open it in your browser, or upload it to any HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages).

> Chat-app previews block outside requests, so searches only work when the file is opened on its own or hosted.

## Search sources

| Tab | Sources |
|---|---|
| Web | Wikipedia, Hacker News |
| Images | Wikimedia Commons |
| Videos | Internet Archive |
| News | Hacker News (tech) |
| Academic | OpenAlex, Crossref |
| Books | Open Library, Internet Archive |
| Code | Stack Overflow, Hacker News |
| Maps | OpenStreetMap |

All sources are free and need no API key. Each one fails on its own without breaking the others.

## How it works

Runs in your browser: query parsing (`"phrases"`, `-exclude`, `site:`), BM25 and TF-IDF ranking, duplicate removal, domain diversity, spelling suggestions, filters, caching and history.

Sent to remote sources: your search text, to the sources used by the tab you are on.

## Privacy

Your history is stored only in your browser and can be cleared in Settings. Each search is sent to that tab's sources, so it is not anonymous to them.

## Limits

- It does not crawl the web. A full web index needs crawlers, storage and backend servers.
- Free sources have rate limits, and some may block browser requests.
- No shopping, language filter or safe search yet.
- One-tap install and offline mode need a real `manifest.json` and `sw.js` hosted beside the HTML.

## Tests

The algorithms have 11 built-in self-tests (Settings, then Run self-test). Provider responses and the install flow are not yet tested against live services.

## Check before you launch

"Velqira" has not been cleared as a trademark or domain. Check before public use.
