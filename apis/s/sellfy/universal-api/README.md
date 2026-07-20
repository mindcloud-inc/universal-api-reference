# <img src="https://images.mindcloud.co/apps/icons/sellfy_1773929864613.png" alt="Sellfy logo" width="28" height="28"> Sellfy: Universal API

Embed Sellfy stores and products on your website

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sellfy/latest
- **Category:** Commerce
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sellfy.com
- **Vendor API docs:** https://docs.sellfy.com/article/348-oembed

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get oEmbed](actions/get-oembed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fdemo.sellfy.store%2Fp%2Fbottle-mockup%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Embed

| Action | Method | Description |
| --- | --- | --- |
| [Get oEmbed](actions/get-oembed.md) | GET | Retrieves oEmbed data from Sellfy for a store or product URL. |

