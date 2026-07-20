# <img src="https://images.mindcloud.co/apps/icons/background-cut_1776195227699.png" alt="BackgroundCut logo" width="28" height="28"> BackgroundCut: Universal API

BackgroundCut removes image backgrounds with AI and returns either a processed image URL or a generated PNG/WEBP cutout depending on the API version and input mode.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/backgroundCut/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://backgroundcut.co/
- **Vendor API docs:** https://backgroundcut.co/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Alpha Mask From Base64 (v2)](actions/generate-alpha-mask-from-base64-v2.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageFileB64": "string"
}'
```

## Actions (6)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate Alpha Mask From Base64 (v2)](actions/generate-alpha-mask-from-base64-v2.md) | POST | Generates an alpha mask in BackgroundCut from a base64 image. |
| [Generate Alpha Mask From File (v2)](actions/generate-alpha-mask-from-file-v2.md) | POST | Generates an alpha mask in BackgroundCut from an uploaded file. |
| [Remove Background From Base64 (v2)](actions/remove-background-from-base64-v2.md) | POST | Removes an image background in BackgroundCut from a base64 image. |
| [Remove Background From File (v1)](actions/remove-background-from-file-v1.md) | POST | Removes an image background in BackgroundCut from an uploaded file. |
| [Remove Background From File (v2)](actions/remove-background-from-file-v2.md) | POST | Removes an image background in BackgroundCut from an uploaded file. |
| [Remove Background From Image URL (v1)](actions/remove-background-from-image-url-v1.md) | POST | Removes an image background in BackgroundCut from an image URL. |

