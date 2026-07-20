# <img src="https://images.mindcloud.co/apps/icons/favicon-support-cartloom-com-48x48-1_1777044517412.png" alt="Cartloom logo" width="28" height="28"> Cartloom: Universal API

Cartloom is an ecommerce platform for selling physical and digital products, managing orders, and creating discount codes through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cartloom/latest
- **Category:** Commerce
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cartloom.com
- **Vendor API docs:** https://support.cartloom.com/hc/en-us/sections/115000264307-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Discount](actions/get-discount.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [Add Discount](actions/add-discount.md) | POST | Creates a new discount in Cartloom. |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a discount record from Cartloom by ID. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves multiple discount records from Cartloom. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Cartloom by invoice number. |
| [List Orders](actions/list-orders.md) | GET | Retrieves multiple order records from Cartloom. |

