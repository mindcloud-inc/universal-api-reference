# <img src="https://images.mindcloud.co/apps/icons/alt-text-ai-icon_1777060251904.png" alt="AltText.Ai logo" width="28" height="28"> AltText.Ai: Universal API

Generate, search, and manage AI-generated alt text for images in your AltText.ai library.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/altTextAi/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://alttext.ai/
- **Vendor API docs:** https://alttext.ai/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Images](actions/list-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/list-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your account settings from AltText.Ai. |
| [Update Account](actions/update-account.md) | PUT | Updates your account settings in AltText.Ai. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upload Images](actions/bulk-upload-images.md) | POST | Bulk uploads image URLs for alt text generation in AltText.Ai. |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an image from your AltText.Ai library. |
| [Generate Alt Text for Image](actions/generate-alt-text-for-image.md) | POST | Generates alt text for a new image in AltText.Ai. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image from your AltText.Ai library. |
| [List Images](actions/list-images.md) | GET | Retrieves images from your AltText.Ai library. |
| [Scrape Page Images](actions/scrape-page-images.md) | POST | Scrapes page images for alt text generation in AltText.Ai. |
| [Search Images](actions/search-images.md) | GET | Searches images in your AltText.Ai library. |
| [Update Image](actions/update-image.md) | PUT | Updates an image in your AltText.Ai library. |

