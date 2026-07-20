# <img src="https://images.mindcloud.co/apps/icons/goldbelly_1778006461646.png" alt="Goldbelly logo" width="28" height="28"> Goldbelly: Universal API

Goldbelly 3PL API wrapper for orders, tracking, product inventory, subproduct inventory, and gift cards.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goldbelly/latest
- **Category:** Commerce
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.goldbelly.com
- **Vendor API docs:** https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Gift Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Gift Card](actions/create-gift-card.md) | POST |  |
| [Debit Gift Card](actions/debit-gift-card.md) | PUT |  |
| [Get Gift Card](actions/get-gift-card.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Orders](actions/bulk-update-orders.md) | PUT |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Subproducts](actions/bulk-update-subproducts.md) | PUT |  |
| [List Subproducts](actions/list-subproducts.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Products](actions/bulk-update-products.md) | PUT |  |
| [List Products](actions/list-products.md) | GET |  |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking](actions/get-tracking.md) | GET |  |

