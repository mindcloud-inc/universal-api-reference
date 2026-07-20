# <img src="https://images.mindcloud.co/apps/icons/phandomjs_1777063879504.png" alt="PhantomJsCloud logo" width="28" height="28"> PhantomJsCloud: Universal API

PhantomJsCloud: Render pages, automate browsers, and capture outputs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phantomJsCloud/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://phantomjscloud.com
- **Vendor API docs:** https://phantomjscloud.com/docs/http-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Render Page as Text](actions/render-page-as-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/render-page-as-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Render Page as HTML](actions/render-page-as-html.md) | GET | Renders a page as HTML in PhantomJsCloud. |
| [Render Page as PDF](actions/render-page-as-pdf.md) | GET | Renders a page as PDF in PhantomJsCloud. |
| [Render Page as Text](actions/render-page-as-text.md) | GET | Renders a page as plain text in PhantomJsCloud. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot as JPEG](actions/capture-screenshot-as-jpeg.md) | GET | Captures a page screenshot as JPEG in PhantomJsCloud. |
| [Capture Screenshot as PNG](actions/capture-screenshot-as-png.md) | GET | Captures a page screenshot as PNG in PhantomJsCloud. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Run Browser Automation](actions/run-browser-automation.md) | GET | Runs browser automation in PhantomJsCloud. |

