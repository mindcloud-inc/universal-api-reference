# <img src="https://images.mindcloud.co/apps/icons/browserless_1774286440330.png" alt="Browserless logo" width="28" height="28"> Browserless: Universal API

Run browser automation and capture content, screenshots, PDFs, and downloads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/browserless/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.browserless.io
- **Vendor API docs:** https://docs.browserless.io/rest-apis/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Web](actions/search-web.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Content](actions/get-page-content.md) | GET | Retrieves rendered page content from Browserless. |
| [Smart Scrape Url](actions/smart-scrape-url.md) | GET | Retrieves structured page data from a URL in Browserless. |

### Downloaded File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file through Browserless browser automation. |

### Exported Resource

| Action | Method | Description |
| --- | --- | --- |
| [Export Url](actions/export-url.md) | GET | Downloads a URL in its native format from Browserless. |

### Function Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Browser Function](actions/run-browser-function.md) | GET | Runs custom browser code in Browserless. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Map Site Links](actions/map-site-links.md) | GET | Retrieves discovered site links from Browserless. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate Pdf](actions/generate-pdf.md) | GET | Generates a PDF from a page in Browserless. |

### Performance Audit

| Action | Method | Description |
| --- | --- | --- |
| [Run Performance Audit](actions/run-performance-audit.md) | GET | Retrieves Lighthouse audit results from Browserless. |

### Scrape Result

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Page Data](actions/scrape-page-data.md) | GET | Retrieves structured page data from Browserless using selectors. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | GET | Captures a page screenshot in Browserless. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Web](actions/search-web.md) | GET | Retrieves web search results from Browserless. |

### Unblocked Page

| Action | Method | Description |
| --- | --- | --- |
| [Unblock Url](actions/unblock-url.md) | GET | Retrieves page content from blocked sites in Browserless. |

