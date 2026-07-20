# <img src="https://images.mindcloud.co/apps/icons/deep-ai_1782742269900.png" alt="DeepAI logo" width="28" height="28"> DeepAI: Universal API

DeepAI provides AI image generation and image editing endpoints including text-to-image, background removal, colorization, upscaling, image replacement, and image expansion.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://deepai.org
- **Vendor API docs:** https://api.deepai.org/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Colorize Image](actions/colorize-image.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepAI/latest/actions/colorize-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "https://example.com/image.jpg"
}'
```

## Actions (9)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Colorize Image](actions/colorize-image.md) | POST | Creates a colorized image in DeepAI. |
| [Creative Upscale](actions/creative-upscale.md) | POST | Creates a creatively upscaled image in DeepAI. |
| [Edit Image](actions/edit-image.md) | POST | Creates an edited image from a prompt in DeepAI. |
| [Expand Image](actions/expand-image.md) | POST |  |
| [Generate Image](actions/generate-image.md) | POST | Creates an AI-generated image in DeepAI. |
| [Remove Background](actions/remove-background.md) | POST | Creates an image with the background removed in DeepAI. |
| [Replace Image Region](actions/replace-image-region.md) | POST | Creates an edited image by replacing a masked region in DeepAI. |
| [Upscale Anime Image](actions/upscale-anime-image.md) | POST | Creates a denoised, upscaled image in DeepAI. |
| [Upscale Image](actions/upscale-image.md) | POST | Creates a sharper, upscaled image in DeepAI. |

