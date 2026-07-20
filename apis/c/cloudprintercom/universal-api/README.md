# <img src="https://images.mindcloud.co/apps/icons/cloudprintercom_1774908099930.png" alt="Cloudprinter.com logo" width="28" height="28"> Cloudprinter.com: Universal API

Quote, place, track, and cancel print orders with Cloudprinter.com, and browse products and shipping options through the Cloudprinter Core API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudprintercom/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cloudprinter.com/
- **Vendor API docs:** https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Add Order](actions/add-order.md) | POST | Creates an order in Cloudprinter.com. |
| [Cancel Order](actions/cancel-order.md) | PUT | Cancels an order in Cloudprinter.com. |
| [Get Order Info](actions/get-order-info.md) | GET | Retrieves order details from Cloudprinter.com. |
| [Get Order Log](actions/get-order-log.md) | GET | Retrieves an order log from Cloudprinter.com. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Cloudprinter.com. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Info](actions/get-product-info.md) | GET | Retrieves product details from Cloudprinter.com. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Cloudprinter.com. |

### Request For Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Quote](actions/get-order-quote.md) | GET | Retrieves an order quote from Cloudprinter.com. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Countries](actions/list-shipping-countries.md) | GET | Retrieves shipping countries from Cloudprinter.com. |
| [List Shipping Levels](actions/list-shipping-levels.md) | GET | Retrieves shipping levels from Cloudprinter.com. |
| [List Shipping States](actions/list-shipping-states.md) | GET | Retrieves shipping states from Cloudprinter.com. |

