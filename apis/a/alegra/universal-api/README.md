# <img src="https://images.mindcloud.co/apps/icons/alegra_1773666836795.png" alt="Alegra logo" width="28" height="28"> Alegra: Universal API

Alegra: manage contacts, items, sales invoices, bills, payments, company info, and webhook subscriptions from the Alegra API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alegra/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.alegra.com
- **Vendor API docs:** https://developer.alegra.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | POST | Creates a new purchase bill in Alegra. |
| [Get Bill](actions/get-bill.md) | GET | Retrieves a purchase bill from Alegra. |
| [List Bills](actions/list-bills.md) | GET | Retrieves purchase bills from your Alegra account. |
| [Update Bill](actions/update-bill.md) | PUT | Updates an existing purchase bill in Alegra. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from your Alegra account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Alegra. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Alegra. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from your Alegra account. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Alegra account. |
| [Restore Contact](actions/restore-contact.md) | PUT | Restores a deleted contact in Alegra. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Alegra. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new sales invoice in Alegra. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing sales invoice from Alegra. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves a sales invoice from Alegra. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves sales invoices from your Alegra account. |
| [Send Invoice Email](actions/send-invoice-email.md) | POST | Sends a sales invoice by email from Alegra. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing sales invoice in Alegra. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Alegra. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Alegra. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from your Alegra account. |
| [List Items](actions/list-items.md) | GET | Retrieves items from your Alegra account. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Alegra. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in Alegra. |
| [Delete Payment](actions/delete-payment.md) | DELETE | Deletes an existing payment from Alegra. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from your Alegra account. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from your Alegra account. |
| [Update Payment](actions/update-payment.md) | PUT | Updates an existing payment in Alegra. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Alegra. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from Alegra. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from your Alegra account. |

