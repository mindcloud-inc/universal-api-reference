# <img src="https://images.mindcloud.co/apps/icons/a-pimage_1774994982547.png" alt="APImage logo" width="28" height="28"> APImage: Universal API

APImage is an AI image generation and editing platform with a unified Image Studio API for prompt enhancement, image generation, and background removal.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aPImage/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apimage.org
- **Vendor API docs:** https://apimage.org/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze Image](actions/analyze-image.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPImage/latest/actions/analyze-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image_url": "https://example.com/image.png",
  "prompt": "List the objects and text visible in the image."
}'
```

## Actions (4)

### Background Removal

| Action | Method | Description |
| --- | --- | --- |
| [Remove Background](actions/remove-background.md) | POST | Removes the background from an image with APImage. |

### Image Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Image](actions/analyze-image.md) | POST | Extracts text from an image with APImage. |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Generates or edits an image with APImage. |

### Prompt Enhancement

| Action | Method | Description |
| --- | --- | --- |
| [Enhance Prompt](actions/enhance-prompt.md) | POST | Rewrites a prompt for AI image generation in APImage. |

