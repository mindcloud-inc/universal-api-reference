# <img src="https://images.mindcloud.co/apps/icons/gumroad_1773241473406.png" alt="Gumroad logo" width="28" height="28"> Gumroad: Universal API

Sell products and manage Gumroad sales

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gumroad/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gumroad.com
- **Vendor API docs:** https://gumroad.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Gumroad. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from Gumroad. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields for a Gumroad product. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in Gumroad. |

### Offer Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer Code](actions/create-offer-code.md) | POST | Creates a new offer code in Gumroad. |
| [Delete Offer Code](actions/delete-offer-code.md) | DELETE | Deletes an existing offer code from Gumroad. |
| [Get Offer Code](actions/get-offer-code.md) | GET | Retrieves an offer code from Gumroad. |
| [List Offer Codes](actions/list-offer-codes.md) | GET | Retrieves offer codes for a Gumroad product. |
| [Update Offer Code](actions/update-offer-code.md) | PUT | Updates an existing offer code in Gumroad. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Get Payout](actions/get-payout.md) | GET | Retrieves a payout from Gumroad. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from Gumroad. |
| [List Upcoming Payouts](actions/list-upcoming-payouts.md) | GET | Retrieves upcoming payouts from Gumroad. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Disable Product](actions/disable-product.md) | PUT | Disables a product in Gumroad. |
| [Enable Product](actions/enable-product.md) | PUT | Enables a product in Gumroad. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Gumroad. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Gumroad. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale](actions/get-sale.md) | GET | Retrieves a sale from Gumroad. |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Gumroad. |
| [Mark Sale as Shipped](actions/mark-sale-as-shipped.md) | PUT | Marks a sale as shipped in Gumroad. |
| [Refund Sale](actions/refund-sale.md) | PUT | Refunds a sale in Gumroad. |
| [Resend Sale Receipt](actions/resend-sale-receipt.md) | POST | Resends a sale receipt from Gumroad. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Gumroad. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers for a Gumroad product. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from Gumroad. |

