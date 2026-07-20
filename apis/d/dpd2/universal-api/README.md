# <img src="https://images.mindcloud.co/apps/icons/gedpdp_1776793983774.jpeg" alt="Dpd2 logo" width="28" height="28"> Dpd2: Universal API

Access your DPD account data, including storefronts, products, purchases, subscribers, and customers, with support for purchase reactivation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dpd2/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getdpd.com
- **Vendor API docs:** https://getdpd.com/docs/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Retrieves API ping status from DPD. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from DPD by ID. |
| [List Products](actions/list-products.md) | GET | Retrieves products from DPD, optionally filtered by storefront. |

### Storefront

| Action | Method | Description |
| --- | --- | --- |
| [Get Storefront](actions/get-storefront.md) | GET | Retrieves a storefront from DPD by ID. |
| [List Storefronts](actions/list-storefronts.md) | GET | Retrieves storefronts from your DPD account. |

