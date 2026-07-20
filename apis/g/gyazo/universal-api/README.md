# <img src="https://images.mindcloud.co/apps/icons/gyazo-icon_1775760185283.png" alt="Gyazo logo" width="28" height="28"> Gyazo: Universal API

Gyazo is an image and screen capture sharing service. Connect Gyazo to list, search, upload, inspect, and delete images from a user account.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gyazo/latest
- **Category:** Marketing / Social Media
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gyazo.com
- **Vendor API docs:** https://gyazo.com/api/docs/user

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an existing image from Gyazo. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image from Gyazo. |
| [Get Image OEmbed](actions/get-image-o-embed.md) | GET | Retrieves oEmbed data for a Gyazo image. |
| [List Images](actions/list-images.md) | GET | Retrieves images from Gyazo. |
| [Search Images](actions/search-images.md) | GET | Finds images in Gyazo by search query. |
| [Upload Image](actions/upload-image.md) | POST | Uploads a new image to Gyazo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Gyazo. |

