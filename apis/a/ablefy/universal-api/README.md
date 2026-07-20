# <img src="https://images.mindcloud.co/apps/icons/ablefy_1773257749589.png" alt="Ablefy logo" width="28" height="28"> Ablefy: Universal API

Sell digital products, courses, memberships, coaching, and community access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ablefy/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ablefy.io/
- **Vendor API docs:** https://api.myablefy.com/api/swagger_doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your account details from Ablefy. |

### Funnel

| Action | Method | Description |
| --- | --- | --- |
| [Create Funnel](actions/create-funnel.md) | POST | Creates a new funnel in Ablefy. |
| [Delete Funnel](actions/delete-funnel.md) | DELETE | Deletes an existing funnel from Ablefy. |
| [Get Funnel](actions/get-funnel.md) | GET | Retrieves a funnel from Ablefy. |
| [List Funnels](actions/list-funnels.md) | GET | Retrieves funnels from Ablefy. |
| [Update Funnel](actions/update-funnel.md) | PUT | Updates an existing funnel in Ablefy. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Ablefy. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Updates an order in Ablefy by canceling it. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Ablefy. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Ablefy. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from Ablefy. |
| [Refund Payment](actions/refund-payment.md) | PUT | Updates a payment in Ablefy by refunding it. |

### Pricing Plan

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pricing Plan](actions/delete-pricing-plan.md) | DELETE | Deletes an existing pricing plan from Ablefy. |
| [Get Pricing Plan](actions/get-pricing-plan.md) | GET | Retrieves a pricing plan from Ablefy. |
| [List Pricing Plans](actions/list-pricing-plans.md) | GET | Retrieves pricing plans from Ablefy. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Ablefy. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Ablefy. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Ablefy. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Ablefy. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a new webhook endpoint in Ablefy. |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE | Deletes an existing webhook endpoint from Ablefy. |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Ablefy. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from Ablefy. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates an existing webhook endpoint in Ablefy. |

