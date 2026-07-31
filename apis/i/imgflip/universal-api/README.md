# <img src="https://images.mindcloud.co/apps/icons/imgflip_1785426368457.png" alt="Imgflip logo" width="28" height="28"> Imgflip: Universal API

List popular Imgflip templates and create publicly accessible captioned images with a dedicated account.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imgflip/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://imgflip.com/
- **Vendor API docs:** https://imgflip.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Popular Memes](actions/list-popular-memes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Meme

| Action | Method | Description |
| --- | --- | --- |
| [List Popular Memes](actions/list-popular-memes.md) | GET |  |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Caption Image](actions/caption-image.md) | POST |  |

