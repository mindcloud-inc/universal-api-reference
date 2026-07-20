# <img src="https://images.mindcloud.co/apps/icons/html-css-to-image-icon_1773426019170.png" alt="HTML/CSS to Image app logo" width="28" height="28"> HTML/CSS to Image app: Universal API

Generate images, screenshots, PDFs, and reusable templates from HTML and CSS using the HTML/CSS to Image API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hTMLCSSToImageApp/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://htmlcsstoimage.com
- **Vendor API docs:** https://docs.htmlcsstoimage.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST |  |
| [Delete Image](actions/delete-image.md) | DELETE |  |
| [Delete Images Batch](actions/delete-images-batch.md) | DELETE |  |
| [Get Image](actions/get-image.md) | GET |  |
| [Render Template](actions/render-template.md) | POST |  |
| [Render Template Version](actions/render-template-version.md) | POST |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [List Template Versions](actions/list-template-versions.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET |  |

