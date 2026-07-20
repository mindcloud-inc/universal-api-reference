# <img src="https://images.mindcloud.co/apps/icons/screenshot-api_1774272884767.png" alt="ScreenshotAPI logo" width="28" height="28"> ScreenshotAPI: Universal API

Capture, extract, and automate website screenshots and web content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/screenshotAPI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.screenshotapi.net
- **Vendor API docs:** https://www.screenshotapi.net/docs/getStarted

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract HTML](actions/extract-html.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotAPI/latest/actions/extract-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

## Actions (8)

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Extract HTML](actions/extract-html.md) | POST | Creates extracted page HTML in ScreenshotAPI. |
| [Extract Text](actions/extract-text.md) | POST | Creates extracted page text in ScreenshotAPI. |
| [Generate PDF](actions/generate-pdf.md) | POST | Creates a new PDF capture in ScreenshotAPI. |
| [Record Multiple Scrolling Screenshots](actions/record-multiple-scrolling-screenshots.md) | POST | Creates multiple scrolling screenshot recordings in ScreenshotAPI. |
| [Record Scrolling Screenshot](actions/record-scrolling-screenshot.md) | POST | Creates a scrolling screenshot recording in ScreenshotAPI. |
| [Render Custom HTML](actions/render-custom-html.md) | POST | Creates a screenshot from custom HTML in ScreenshotAPI. |
| [Render Screenshot](actions/render-screenshot.md) | POST | Creates a new PNG screenshot in ScreenshotAPI. |
| [Render Screenshot JSON](actions/render-screenshot-json.md) | POST | Creates screenshot metadata in ScreenshotAPI with selectable file output. |

