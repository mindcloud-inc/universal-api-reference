# <img src="https://images.mindcloud.co/apps/icons/gift-up_1773943631663.png" alt="Gift Up logo" width="28" height="28"> Gift Up: Universal API

Sell, manage, and redeem digital gift cards and vouchers through Gift Up.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/giftUp/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.giftup.com
- **Vendor API docs:** https://developer.giftup.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Gift Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Gift Card by Code](actions/get-gift-card-by-code.md) | GET |  |
| [List Gift Cards](actions/list-gift-cards.md) | GET |  |
| [Reactivate Gift Card](actions/reactivate-gift-card.md) | PUT |  |
| [Redeem Gift Card](actions/redeem-gift-card.md) | PUT |  |
| [Redeem Gift Card in Full](actions/redeem-gift-card-in-full.md) | PUT |  |
| [Top Up Gift Card](actions/top-up-gift-card.md) | PUT |  |
| [Undo Gift Card Redemption](actions/undo-gift-card-redemption.md) | PUT |  |
| [Update Gift Card](actions/update-gift-card.md) | PUT |  |
| [Void Gift Card](actions/void-gift-card.md) | PUT |  |

### Gift Card Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Gift Card Balances](actions/transfer-gift-card-balances.md) | PUT |  |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Get Item by ID](actions/get-item-by-id.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Item Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Group](actions/create-item-group.md) | POST |  |
| [Get Item Group by ID](actions/get-item-group-by-id.md) | GET |  |
| [List Item Groups](actions/list-item-groups.md) | GET |  |
| [Update Item Group](actions/update-item-group.md) | PUT |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order by ID](actions/get-order-by-id.md) | GET |  |

### Report Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Transaction](actions/get-report-transaction.md) | GET |  |
| [List Report Transactions](actions/list-report-transactions.md) | GET |  |

