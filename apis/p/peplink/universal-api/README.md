# <img src="https://images.mindcloud.co/apps/icons/peplink-icon_1782394158080.png" alt="Peplink logo" width="28" height="28"> Peplink: Universal API

Extend your router’s capabilities and enable outdoor use.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peplink/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Products](actions/list-all-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/list-all-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Check Devices](actions/check-devices.md) | GET |  |
| [Create Order](actions/create-order.md) | POST |  |
| [Create Order PO File](actions/create-order-po-file.md) | POST | Create a customer PO File for an order. |
| [Get Order](actions/get-order.md) | GET |  |
| [List All Products](actions/list-all-products.md) | GET |  |
| [Search Devices](actions/search-devices.md) | GET |  |
| [Update customer PO number](actions/update-customer-po-number.md) | POST | Update customer PO number for an order. |

