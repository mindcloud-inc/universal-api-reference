# <img src="https://images.mindcloud.co/apps/icons/e-junkie_1774466233124.png" alt="E-junkie logo" width="28" height="28"> E-junkie: Universal API

Access the documented E-junkie Products API to read seller product catalog data from a connected account.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eJunkie/latest
- **Category:** Commerce
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.e-junkie.com
- **Vendor API docs:** https://www.e-junkie.com/wiki/help-products-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eJunkie/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves product details from an E-junkie catalog. |

