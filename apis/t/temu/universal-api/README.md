# <img src="https://images.mindcloud.co/apps/icons/temu_1782742365236.png" alt="Temu logo" width="28" height="28"> Temu: Universal API

Temu through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/temu/latest
- **Category:** Commerce
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Combined Shipping Groups](actions/get-combined-shipping-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Combined Shipping Groups](actions/get-combined-shipping-groups.md) | GET | Retrieve combined shipping groups including lists of parent orders that can be combined for shipping. |
| [Get Order](actions/get-order.md) | GET | Retrieve detailed information about a specific order. |
| [Get Order Address](actions/get-order-address.md) | GET | Retrieve shipping address information for a specific order. |
| [Get Order Customization](actions/get-order-customization.md) | GET | Retrieve customized product content information in bulk |
| [List Orders](actions/list-orders.md) | GET | List orders with optional filters |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Local SKUs](actions/list-local-sk-us.md) | GET | Search the local SKU list |

