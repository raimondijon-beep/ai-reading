# AI & Agentic AI Reading Dashboard

A single-file dashboard that launches your AI reading list directly in **Readwise Reader** (deep links), with per-item progress and notes saved locally in your browser.

**Live site:** `https://<your-username>.github.io/ai-reading/`  
**Status:** MVP (`v1.0.0`)

---

## Features
- One-page list of PDFs and web resources.
- **Deep links** that open the exact document in the **Reader app** on:
  - **iPad/iOS:** `wiseread://open/private://read/<DOC_ID>`
  - **macOS:** `wiseread://read/<DOC_ID>`
- Per-item **Mark read / unread**, **notes**, and an overall summary.
- **Local storage**—your progress & notes are saved in the browser (per domain).

> Tip: The page also falls back to the web on iOS if the app doesn’t deep-jump.

---

## Add a new item

Open `index.html` and find the `ITEMS` array. Add entries using this pattern:

```js
// PDF (Reader)
{ id: 'unique-id', order: 16, title: 'Title here', type: 'pdf',
  href: 'https://read.readwise.io/read/<DOC_ID>',  // paste the normal Reader web link
  minutes: 12, tags: ['Agentic'], desc: 'Short one-line summary.' }

// Web article
{ id: 'unique-id-2', order: 17, title: 'Web Title', type: 'web',
  href: 'https://example.com/article', minutes: 8, tags: ['Web'], desc: 'Short summary.' }
