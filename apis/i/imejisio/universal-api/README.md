# <img src="https://images.mindcloud.co/apps/icons/imejisio_1775234149456.png" alt="Imejis.io logo" width="28" height="28"> Imejis.io: Universal API

Template-based image generation API for creating branded images from reusable designs and JSON data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imejisio/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.imejis.io/
- **Vendor API docs:** https://www.imejis.io/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Render Image](actions/render-image.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "HxQGYmW6hKu-HAORyRazt"
}'
```

## Actions (1)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Render Image](actions/render-image.md) | POST | Creates a rendered image in Imejis.io by design ID. |

