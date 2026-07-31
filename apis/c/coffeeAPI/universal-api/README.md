# <img src="https://images.mindcloud.co/apps/icons/coffee-api_1785420743786.png" alt="Coffee API logo" width="28" height="28"> Coffee API: Universal API

Get random coffee images and image URLs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coffeeAPI/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coffee.alexflipnote.dev/
- **Vendor API docs:** https://coffee.alexflipnote.dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Coffee Image](actions/get-random-coffee-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Coffee Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Coffee Image](actions/get-random-coffee-image.md) | GET |  |
| [Get Random Coffee Image URL](actions/get-random-coffee-image-url.md) | GET |  |

