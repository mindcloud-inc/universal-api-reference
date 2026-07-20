# <img src="https://images.mindcloud.co/apps/icons/we-supply_1775145112220.png" alt="WeSupply logo" width="28" height="28"> WeSupply: Universal API

WeSupply helps ecommerce teams power order tracking, shipping updates, returns, delivery estimates, SMS updates, and customer self-service experiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weSupply/latest
- **Category:** Commerce
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wesupplylabs.com
- **Vendor API docs:** https://documenter.getpostman.com/view/11859344/T17AiAYq

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Customer Data](actions/get-customer-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Allowed Country

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Allowed Countries](actions/list-shipping-allowed-countries.md) | GET | Retrieves shipping allowed countries from WeSupply. |

### Customer Data

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customer Data](actions/delete-customer-data.md) | DELETE | Deletes customer data from WeSupply. |
| [Get Customer Data](actions/get-customer-data.md) | GET | Retrieves customer data from WeSupply. |

### Delivery Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Delivery Date Quotes](actions/get-delivery-date-quotes.md) | GET | Retrieves delivery date quotes from WeSupply. |

### Estimated Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get Estimated Delivery By Order ID](actions/get-estimated-delivery-by-order-id.md) | GET | Retrieves estimated delivery details from WeSupply by order ID. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Update Item Details](actions/update-item-details.md) | PUT | Updates item details in WeSupply. |

### Item Update

| Action | Method | Description |
| --- | --- | --- |
| [List Updated Item Details](actions/list-updated-item-details.md) | GET | Retrieves updated item details from WeSupply. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Order By External Order ID](actions/lookup-order-by-external-order-id.md) | GET | Retrieves an order from WeSupply by external order ID. |
| [Lookup Order By Order ID](actions/lookup-order-by-order-id.md) | GET | Retrieves an order from WeSupply by order ID. |
| [Lookup Orders By Customer Email](actions/lookup-orders-by-customer-email.md) | GET | Finds orders in WeSupply by customer email. |

### Order Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Orders](actions/import-orders.md) | POST | Creates orders in WeSupply from an order JSON payload. |

### Order Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Links](actions/get-order-links.md) | GET | Retrieves WeSupply order links for external order IDs. |

### Recent Return

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Returns](actions/list-recent-returns.md) | GET | Retrieves recent returns from WeSupply. |

### Return

| Action | Method | Description |
| --- | --- | --- |
| [Approve Return](actions/approve-return.md) | PUT | Approves an existing return in WeSupply. |
| [Cancel Return](actions/cancel-return.md) | PUT | Cancels an existing return in WeSupply. |
| [Get Return By Customer Email](actions/get-return-by-customer-email.md) | GET | Retrieves a return from WeSupply by customer email. |
| [Get Return By External Order ID](actions/get-return-by-external-order-id.md) | GET | Retrieves a return from WeSupply by external order ID. |
| [Get Return By Order ID](actions/get-return-by-order-id.md) | GET | Retrieves a return from WeSupply by order ID. |
| [Get Return By Reference](actions/get-return-by-reference.md) | GET | Retrieves a return from WeSupply by reference. |
| [List Returns By Page](actions/list-returns-by-page.md) | GET | Retrieves a page of returns from WeSupply. |

### Return Quality Review

| Action | Method | Description |
| --- | --- | --- |
| [Quality Review Return](actions/quality-review-return.md) | PUT | Updates return quality review in WeSupply. |

### Return Refund

| Action | Method | Description |
| --- | --- | --- |
| [Refund Return](actions/refund-return.md) | PUT | Issues a refund for a return in WeSupply. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates a shipment in WeSupply. |

### Shipping Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipping Estimate For One Product](actions/get-shipping-estimate-for-one-product.md) | GET | Retrieves a shipping estimate from WeSupply for one product. |
| [Get Shipping Estimates For Multiple Products](actions/get-shipping-estimates-for-multiple-products.md) | GET | Retrieves shipping estimates from WeSupply for multiple products. |

### Sms Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe To SMS Notifications](actions/subscribe-to-sms-notifications.md) | POST | Subscribes a customer to WeSupply SMS notifications. |
| [Unsubscribe From SMS Notifications](actions/unsubscribe-from-sms-notifications.md) | DELETE | Unsubscribes a customer from WeSupply SMS notifications. |

### Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracker](actions/create-tracker.md) | POST | Creates a shipment tracker in WeSupply. |

