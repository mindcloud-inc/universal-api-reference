# <img src="https://images.mindcloud.co/apps/icons/phemex_1776360235067.png" alt="Phemex logo" width="28" height="28"> Phemex: Universal API

Phemex is a cryptocurrency exchange for spot, futures, margin, wallet, transfer, and market-data operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phemex/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://phemex.com
- **Vendor API docs:** https://phemex-docs.github.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phemex/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Spot Assets](actions/list-spot-assets.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

