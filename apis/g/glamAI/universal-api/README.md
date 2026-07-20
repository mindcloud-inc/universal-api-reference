# <img src="https://images.mindcloud.co/apps/icons/acebbb54-2383-493a-8802-69afc69d02fb-0_1776270990129.png" alt="Glam AI logo" width="28" height="28"> Glam AI: Universal API

Glam AI provides an AI-powered virtual try-on API for generating product try-on images from source and product images, plus supporting metadata such as available filters.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/glamAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.glam.ai
- **Vendor API docs:** https://glam-ai.readme.io/reference/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Filters](actions/get-filters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [Get Filters](actions/get-filters.md) | GET | Retrieves available filters from Glam AI. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Create Generation](actions/create-generation.md) | POST | Creates an image generation in Glam AI. |

### Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation Result](actions/get-generation-result.md) | GET | Retrieves an image generation result from Glam AI. |

### Try-on Generation

| Action | Method | Description |
| --- | --- | --- |
| [Create Try-On Generation](actions/create-try-on-generation.md) | POST | Creates a try-on generation in Glam AI. |

### Try-on Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Try-On Result](actions/get-try-on-result.md) | GET | Retrieves a try-on result from Glam AI. |

### Uploaded Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Image](actions/upload-image.md) | POST | Uploads an image to Glam AI. |

