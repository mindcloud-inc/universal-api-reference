# <img src="https://images.mindcloud.co/apps/icons/place-bear_1785362102781.png" alt="PlaceBear logo" width="28" height="28"> PlaceBear: Universal API

Generate public color or grayscale bear placeholder images at requested dimensions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placeBear/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://placebear.com/
- **Vendor API docs:** https://placebear.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bear Image](actions/get-bear-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placeBear/latest/actions/get-bear-image?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Bear Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Bear Image](actions/get-bear-image.md) | GET |  |
| [Get Grayscale Bear Image](actions/get-grayscale-bear-image.md) | GET |  |

