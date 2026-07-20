# <img src="https://images.mindcloud.co/apps/icons/id-vvk-i193-logos_1773859853284.jpeg" alt="Eduzz logo" width="28" height="28"> Eduzz: Universal API

Manage Eduzz accounts, products, sales, customers, and subscriptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eduzz/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eduzz.com
- **Vendor API docs:** https://developers.eduzz.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Profile](actions/get-account-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Profile](actions/get-account-profile.md) | GET | Retrieves the logged-in user profile from Eduzz. |

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [List Affiliates](actions/list-affiliates.md) | GET | Retrieves affiliates from Eduzz using the provided filters. |

### Chargeback

| Action | Method | Description |
| --- | --- | --- |
| [List Chargebacks](actions/list-chargebacks.md) | GET | Retrieves chargebacks from Eduzz using the provided filters. |

### Checkout Cart

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Cart](actions/create-checkout-cart.md) | POST | Creates a checkout cart in Eduzz. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Eduzz using the provided filters. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Eduzz using the provided filters. |

### Financial Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Statement](actions/get-financial-statement.md) | GET | Retrieves a financial statement from Eduzz using provided filters. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves the producer's products from Eduzz. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Eduzz using the provided filters. |

### Sales Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Summary](actions/get-sales-summary.md) | GET | Retrieves a sales summary from Eduzz using provided filters. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [List Students](actions/list-students.md) | GET | Retrieves students from Eduzz using the provided filters. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Details by Email](actions/get-customer-details-by-email.md) | GET | Retrieves customer details from Eduzz by email address. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscription details from Eduzz for a date range. |

### Transfer

| Action | Method | Description |
| --- | --- | --- |
| [List Transfers](actions/list-transfers.md) | GET | Retrieves transfer details from Eduzz using the provided filters. |

### Webhook Origin

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Origins](actions/list-webhook-origins.md) | GET | Retrieves available webhook origins from Eduzz. |

### Webhook Sample Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Event Sample](actions/get-webhook-event-sample.md) | GET | Retrieves a sample payload for an Eduzz webhook event. |

### Webhook Secret

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Secret](actions/get-webhook-secret.md) | GET | Retrieves the webhook signing secret from Eduzz. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Eduzz. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from Eduzz. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves all webhook subscriptions from Eduzz. |
| [Set Webhook Subscription Status](actions/set-webhook-subscription-status.md) | PUT | Updates the status of a webhook subscription in Eduzz. |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT | Updates an existing webhook subscription in Eduzz. |

### Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Request Webhook Test](actions/request-webhook-test.md) | POST | Requests a test delivery for an Eduzz webhook subscription. |

