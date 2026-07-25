# <img src="https://images.mindcloud.co/apps/icons/cin7core-icon_1782393034829.webp" alt="Cin7 Core logo" width="28" height="28"> Cin7 Core: Universal API

Cin7 Core Inventory API is part of Cin7 Core Inventory web application at https://inventory.dearsystems.com

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cin7core/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cin7.com/solutions/core/
- **Vendor API docs:** https://dearinventory.docs.apiary.io/#

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Sale](actions/get-sale.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale?connectionId=$CONNECTION_ID&ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [Create Carrier](actions/create-carrier.md) | POST |  |
| [List Carriers](actions/list-carriers.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale](actions/get-sale.md) | GET |  |
| [Get Sale Attachment](actions/get-sale-attachments.md) | GET |  |
| [List Sales](actions/list-sales.md) | GET |  |

### Sale Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale Fulfillment](actions/get-sale-fulfillment.md) | GET |  |

### Sale Fulfillment Pack

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale Fulfillment Pack](actions/create-sale-fulfillment-pack.md) | POST |  |
| [Get Sale Fulfillment Pack](actions/get-sale-fulfillment-pack.md) | GET |  |
| [Update Sale Fulfillment Pack](actions/update-sale-fulfillment-pack.md) | PUT |  |

### Sale Fulfillment Pick

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale Fulfillment Pick](actions/create-sale-fulfillment-pick.md) | POST |  |

### Sale Fulfillment Ship

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale Fulfillment Ship](actions/create-sale-fulfillment-ship.md) | POST |  |
| [Get Sale Fulfillment Ship](actions/get-sale-fulfillment-ship.md) | GET |  |
| [Update Sale Fulfillment Ship](actions/update-sale-fulfillment-ship.md) | PUT |  |

### Sale Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale Order](actions/get-sale-order.md) | GET |  |

