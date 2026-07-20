# <img src="https://images.mindcloud.co/apps/icons/image-router-icon_1775855699007.png" alt="ImageRouter logo" width="28" height="28"> ImageRouter: Universal API

Generate images and videos with ImageRouter models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imageRouter/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://imagerouter.io
- **Vendor API docs:** https://docs.imagerouter.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET |  |

### Credit Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Usage By API Key](actions/get-credit-usage-by-api-key.md) | GET |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET |  |
| [List Models](actions/list-models.md) | GET |  |

