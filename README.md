# UTM Link Builder
 
A free, privacy-first UTM link builder with full Arabic (RTL) support. Generate a tracking link for every channel you publish on, so you always know where your visitors come from.
 
You don't need to run ads. If you simply share your link on Facebook, WhatsApp, Instagram, email or a printed QR code, this tool tells you which channel brought each visit.
 
**Live demo:** `https://YOUR-USERNAME.github.io/utm-link-builder/`
 
## Features
 
- **Source-only by default.** Pick where you will share the link and get a ready-to-copy URL for each channel. No campaign name required.
- **Optional publisher name.** Add who is sharing the link (a person, a branch, a partner). It is stored in `utm_content`, so you can see who drove the traffic.
- **Optional campaign name.** Group several links under one goal when you need to.
- **18 built-in channels:** social media, messaging and email, paid ads, and offline (QR code, print, Google Business Profile), plus a custom channel with your own source and medium.
- **Advanced options:** `utm_term` and `utm_content`. If you use both a publisher and a content label, they are merged (for example `ahmed_video_1`).
- **Auto-clean names.** Lowercase, spaces become `_`, so `Facebook` and `facebook` are never counted as two sources.
- **Existing UTM parameters are replaced**, so you never end up with duplicates.
- **Copy one link or all links at once**, with native share on supported devices.
- **Copy history** saved on your device.
- **Responsive** layout with light and dark mode, accessible focus states and reduced-motion support.
- **Private by design.** Everything runs in your browser. Nothing is sent to a server, and data is stored only in `localStorage`.
## Example output
 
```
https://your-site.com/?utm_source=facebook&utm_medium=social&utm_content=ahmed
```
 
| Parameter | Meaning | In this tool |
|---|---|---|
| `utm_source` | Where you shared the link | Required (from the channel you pick) |
| `utm_medium` | Type of channel | Required (set automatically) |
| `utm_campaign` | Campaign or goal | Optional |
| `utm_content` | Publisher or content variant | Optional |
| `utm_term` | Search keyword | Optional |
 
## Usage
 
1. Enter your website URL.
2. Select the channels where you will share it.
3. Optionally add a publisher name and a campaign name.
4. Copy each link and use it only in its own channel.
5. After a few days, open GA4: **Reports → Acquisition → Traffic acquisition**, and change the dimension to **Session source / medium**.
Tip: test a link first and check **Realtime** in GA4 before sharing it publicly.
 
## Run locally
 
It is a single static file with no build step and no dependencies.
 
```bash
git clone https://github.com/YOUR-USERNAME/utm-link-builder.git
cd utm-link-builder
open index.html   # or just double-click the file
```
 
## Deploy
 
**GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root.
 
It also works on any static host (Netlify, Cloudflare Pages, Vercel).
 
## SEO and performance
 
- Descriptive title and meta description, Open Graph and Twitter tags
- JSON-LD structured data (`WebApplication`, `FAQPage`)
- Semantic HTML with `lang="ar"` and `dir="rtl"`
- Single file, no JavaScript libraries
- Font preconnect with `font-display: swap`
- `content-visibility: auto` on the long informational section
After you pick a domain, add a `<link rel="canonical">` and `og:url` pointing to it.
 
## Privacy
 
No analytics, no cookies, no network requests apart from loading the Google Font. Your URL, names and copy history never leave your device. Use the **Clear my data** button to wipe them at any time.
 
## Contributing
 
Issues and pull requests are welcome. Ideas for improvement:
 
- More channels (Snapchat, Pinterest, Threads, Reddit)
- Bulk link generation from a CSV
- Built-in QR code generation
- English and French interface
## License
 
MIT
 
