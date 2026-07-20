# <img src="https://images.mindcloud.co/apps/icons/screenshot-one_1773781879523.png" alt="ScreenshotOne logo" width="28" height="28"> ScreenshotOne: Universal API

Generate screenshots, PDFs, animations, and webpage metadata with ScreenshotOne

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/screenshotOne/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://screenshotone.com
- **Vendor API docs:** https://screenshotone.com/docs/getting-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Extract Page Content](actions/extract-page-content.md) | GET |  |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET |  |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Extract Open Graph Metadata](actions/extract-open-graph-metadata.md) | GET |  |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | GET |  |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Capture Selector Screenshot](actions/capture-selector-screenshot.md) | GET |  |
| [Render HTML](actions/render-html.md) | GET |  |
| [Render Markdown](actions/render-markdown.md) | GET |  |
| [Take Full-Page Screenshot](actions/take-full-page-screenshot.md) | GET |  |
| [Take Screenshot](actions/take-screenshot.md) | GET |  |

### Stored Asset

| Action | Method | Description |
| --- | --- | --- |
| [Store Rendered Asset](actions/store-rendered-asset.md) | GET |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET |  |

