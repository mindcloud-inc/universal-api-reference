# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-31-141658_1774977450236.png" alt="Mythic Text logo" width="28" height="28"> Mythic Text: Universal API

Transform Markdown into polished HTML and channel-specific output for Gmail, Google Docs, WordPress, web pages, and branded content workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mythicText/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mythictext.com
- **Vendor API docs:** https://mythictext.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Connection Check](actions/connection-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/connection-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Connection Check](actions/connection-check.md) | GET |  |
| [Convert Blog Post To HTML](actions/convert-blog-post-to-html.md) | GET |  |
| [Convert Blog Post To WordPress](actions/convert-blog-post-to-word-press.md) | GET |  |
| [Convert Branded Document (Slate Palette)](actions/convert-branded-document-slate-palette.md) | GET |  |
| [Convert Branded Email (Ocean Palette)](actions/convert-branded-email-ocean-palette.md) | GET |  |
| [Convert Branded Newsletter (Sunset Palette)](actions/convert-branded-newsletter-sunset-palette.md) | GET |  |
| [Convert Branded Web Page (Forest Palette)](actions/convert-branded-web-page-forest-palette.md) | GET |  |
| [Convert Campaign Copy To HTML](actions/convert-campaign-copy-to-html.md) | GET |  |
| [Convert Case Study To HTML](actions/convert-case-study-to-html.md) | GET |  |
| [Convert Executive Summary To PDF Layout](actions/convert-executive-summary-to-pdf-layout.md) | GET |  |
| [Convert Knowledge Base Article To HTML](actions/convert-knowledge-base-article-to-html.md) | GET |  |
| [Convert Knowledge Base Article To WordPress](actions/convert-knowledge-base-article-to-word-press.md) | GET |  |
| [Convert Landing Page Copy To HTML](actions/convert-landing-page-copy-to-html.md) | GET |  |
| [Convert Markdown](actions/convert-markdown.md) | GET |  |
| [Convert Markdown To Email](actions/convert-markdown-to-email.md) | GET |  |
| [Convert Markdown To Gmail](actions/convert-markdown-to-gmail.md) | GET |  |
| [Convert Markdown To Google Docs](actions/convert-markdown-to-google-docs.md) | GET |  |
| [Convert Markdown To HTML](actions/convert-markdown-to-html.md) | GET |  |
| [Convert Markdown To Markdown](actions/convert-markdown-to-markdown.md) | GET |  |
| [Convert Markdown To PDF Layout](actions/convert-markdown-to-pdf-layout.md) | GET |  |
| [Convert Markdown To Web](actions/convert-markdown-to-web.md) | GET |  |
| [Convert Markdown To WordPress](actions/convert-markdown-to-word-press.md) | GET |  |
| [Convert Newsletter To Email](actions/convert-newsletter-to-email.md) | GET |  |
| [Convert Newsletter To Gmail](actions/convert-newsletter-to-gmail.md) | GET |  |
| [Convert Newsletter To Google Docs](actions/convert-newsletter-to-google-docs.md) | GET |  |
| [Convert Press Release To HTML](actions/convert-press-release-to-html.md) | GET |  |
| [Convert Product Launch Email To Gmail](actions/convert-product-launch-email-to-gmail.md) | GET |  |
| [Convert Proposal To Google Docs](actions/convert-proposal-to-google-docs.md) | GET |  |
| [Convert Release Notes To Email](actions/convert-release-notes-to-email.md) | GET |  |
| [Convert Sales Enablement Doc To Google Docs](actions/convert-sales-enablement-doc-to-google-docs.md) | GET |  |
| [Convert Web Announcement To Web](actions/convert-web-announcement-to-web.md) | GET |  |

