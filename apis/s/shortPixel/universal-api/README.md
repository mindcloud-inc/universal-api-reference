# <img src="https://images.mindcloud.co/apps/icons/short-pixel-icon-square_1776185936908.png" alt="ShortPixel logo" width="28" height="28"> ShortPixel: Universal API

ShortPixel image optimization API wrapper for reducer, synchronized reducer, and post-reducer operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortPixel/latest
- **Category:** Content & Files / Storage
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shortpixel.com
- **Vendor API docs:** https://shortpixel.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Remote Optimization Status](actions/check-remote-optimization-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/check-remote-optimization-status?connectionId=$CONNECTION_ID&optimizationUrls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Check Remote Optimization Status](actions/check-remote-optimization-status.md) | GET | Retrieves remote image optimization status from ShortPixel. |
| [Check Uploaded Optimization Status](actions/check-uploaded-optimization-status.md) | GET | Retrieves uploaded image optimization status from ShortPixel. |
| [Optimize Remote Image Direct](actions/optimize-remote-image-direct.md) | POST | Creates an optimized image directly from a remote URL in ShortPixel. |
| [Optimize Remote Images](actions/optimize-remote-images.md) | POST | Creates optimized image results from remote URLs in ShortPixel. |
| [Optimize Uploaded Images](actions/optimize-uploaded-images.md) | POST | Creates optimized image results from uploaded files in ShortPixel. |

