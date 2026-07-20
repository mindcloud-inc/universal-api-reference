# <img src="https://images.mindcloud.co/apps/icons/money-bird_1773333158308.png" alt="MoneyBird logo" width="28" height="28"> MoneyBird: Universal API

Manage contacts, invoices, estimates, products, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moneyBird/latest
- **Category:** Commerce / Accounting
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moneybird.com/
- **Vendor API docs:** https://developer.moneybird.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Administrations](actions/list-administrations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [List Administrations](actions/list-administrations.md) | GET | Retrieves administrations from MoneyBird. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in MoneyBird. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from MoneyBird. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from MoneyBird. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in MoneyBird. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create General Document](actions/create-general-document.md) | POST | Creates a new general document in MoneyBird. |
| [Get General Document](actions/get-general-document.md) | GET | Retrieves a general document from MoneyBird. |
| [List General Documents](actions/list-general-documents.md) | GET | Retrieves general documents from MoneyBird. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Invoice](actions/create-sales-invoice.md) | POST | Creates a new sales invoice in MoneyBird. |
| [Get Sales Invoice](actions/get-sales-invoice.md) | GET | Retrieves a sales invoice from MoneyBird. |
| [List Sales Invoices](actions/list-sales-invoices.md) | GET | Retrieves sales invoices from MoneyBird. |
| [Send Sales Invoice](actions/send-sales-invoice.md) | PUT | Sends an existing sales invoice from MoneyBird. |
| [Update Sales Invoice](actions/update-sales-invoice.md) | PUT | Updates an existing sales invoice in MoneyBird. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in MoneyBird. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from MoneyBird. |
| [List Products](actions/list-products.md) | GET | Retrieves products from MoneyBird. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in MoneyBird. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in MoneyBird. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from MoneyBird. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from MoneyBird. |
| [Send Estimate](actions/send-estimate.md) | PUT | Sends an existing estimate from MoneyBird. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an existing estimate in MoneyBird. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in MoneyBird. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from MoneyBird. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in MoneyBird. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from MoneyBird. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from MoneyBird. |

