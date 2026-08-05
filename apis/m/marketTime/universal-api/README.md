# <img src="https://images.mindcloud.co/apps/icons/market-time_1785515137425.png" alt="MarketTime logo" width="28" height="28"> MarketTime: Universal API

Manage MarketTime orders, inventory, customers, items, and shipments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/marketTime/latest
- **Category:** Commerce
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.markettime.com/
- **Vendor API docs:** https://publicapi.markettime.com/swagger-ui/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Item Inventory](actions/get-item-inventory.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/get-item-inventory?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Item Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Inventory](actions/get-item-inventory.md) | GET |  |
| [List Item Inventory](actions/list-item-inventory.md) | GET |  |
| [Update Item Inventory](actions/update-item-inventory.md) | PUT |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Pull Orders](actions/pull-orders.md) | GET |  |

