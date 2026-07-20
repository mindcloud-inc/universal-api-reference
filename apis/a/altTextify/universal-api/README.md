# <img src="https://images.mindcloud.co/apps/icons/alt-textify_1776082367251.png" alt="AltTextify logo" width="28" height="28"> AltTextify: Universal API

AI-powered alt text generation service for images, with upload, retrieval, job lookup, and deletion endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/altTextify/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://alttextify.net/
- **Vendor API docs:** https://apidoc.alttextify.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Images](actions/list-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/list-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an image from AltTextify by asset ID. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image from AltTextify by asset ID. |
| [List Images](actions/list-images.md) | GET | Retrieves all account images from AltTextify. |
| [Upload Image From URL](actions/upload-image-from-url.md) | POST | Creates a new image in AltTextify from an image URL. |
| [Upload Raw Image](actions/upload-raw-image.md) | POST | Creates a new image in AltTextify from base64 image data. |

