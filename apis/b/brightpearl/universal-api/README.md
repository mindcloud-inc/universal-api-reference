# <img src="https://images.mindcloud.co/apps/icons/brightpearl_1794931950356.png" alt="Brightpearl logo" width="28" height="28"> Brightpearl: Universal API

Manage orders, inventory, stock corrections, and warehouse fulfilment

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brightpearl/latest
- **Category:** Commerce / ERP
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.brightpearl.com
- **Vendor API docs:** https://api-docs.brightpearl.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Goods-in Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Goods-In Note](actions/create-goods-in-note.md) | POST |  |
| [Delete Goods-In Note](actions/delete-goods-in-note.md) | DELETE |  |
| [List Goods-In Notes](actions/list-goods-in-notes.md) | GET |  |
| [List Goods-In Notes by ID](actions/list-goods-in-notes-by-id.md) | GET |  |

### Goods-out Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Goods-Out Notes](actions/create-goods-out-notes.md) | POST |  |
| [Delete Goods-Out Note](actions/delete-goods-out-note.md) | DELETE |  |
| [List Goods-Out Notes](actions/list-goods-out-notes.md) | GET |  |
| [List Goods-Out Notes by ID](actions/list-goods-out-notes-by-id.md) | GET |  |
| [Update Goods-Out Note](actions/update-goods-out-note.md) | PUT |  |

### Goods-out Note Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Goods-Out Note Events](actions/add-goods-out-note-events.md) | POST |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [List Orders by ID](actions/list-orders-by-id.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |

### Product Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Product Availability](actions/list-product-availability.md) | GET |  |

### Stock Correction

| Action | Method | Description |
| --- | --- | --- |
| [Create Stock Corrections](actions/create-stock-corrections.md) | POST |  |
| [List Stock Corrections by ID](actions/list-stock-corrections-by-id.md) | GET |  |

