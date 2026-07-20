# Mythic Text: Native API Reference

A consolidated summary of Mythic Text's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://mythictext.com/docs
- **API base URL:** `https://mythictext-api.vercel.app`

## Authentication

### X-API-Key Header

Authenticate Mythic Text by sending your API key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required · Your Mythic Text API key.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://mythictext.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connection Check](actions/connection-check.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Blog Post To HTML](actions/convert-blog-post-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Blog Post To WordPress](actions/convert-blog-post-to-word-press.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Branded Document (Slate Palette)](actions/convert-branded-document-slate-palette.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Branded Email (Ocean Palette)](actions/convert-branded-email-ocean-palette.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Branded Newsletter (Sunset Palette)](actions/convert-branded-newsletter-sunset-palette.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Branded Web Page (Forest Palette)](actions/convert-branded-web-page-forest-palette.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Campaign Copy To HTML](actions/convert-campaign-copy-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Case Study To HTML](actions/convert-case-study-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Executive Summary To PDF Layout](actions/convert-executive-summary-to-pdf-layout.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Knowledge Base Article To HTML](actions/convert-knowledge-base-article-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Knowledge Base Article To WordPress](actions/convert-knowledge-base-article-to-word-press.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Landing Page Copy To HTML](actions/convert-landing-page-copy-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown](actions/convert-markdown.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To Email](actions/convert-markdown-to-email.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To Gmail](actions/convert-markdown-to-gmail.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To Google Docs](actions/convert-markdown-to-google-docs.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To HTML](actions/convert-markdown-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To Markdown](actions/convert-markdown-to-markdown.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To PDF Layout](actions/convert-markdown-to-pdf-layout.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To Web](actions/convert-markdown-to-web.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Markdown To WordPress](actions/convert-markdown-to-word-press.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Newsletter To Email](actions/convert-newsletter-to-email.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Newsletter To Gmail](actions/convert-newsletter-to-gmail.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Newsletter To Google Docs](actions/convert-newsletter-to-google-docs.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Press Release To HTML](actions/convert-press-release-to-html.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Product Launch Email To Gmail](actions/convert-product-launch-email-to-gmail.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Proposal To Google Docs](actions/convert-proposal-to-google-docs.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Release Notes To Email](actions/convert-release-notes-to-email.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Sales Enablement Doc To Google Docs](actions/convert-sales-enablement-doc-to-google-docs.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
| [Convert Web Announcement To Web](actions/convert-web-announcement-to-web.md) | `POST /convert` | [docs](https://mythictext.com/docs) |
