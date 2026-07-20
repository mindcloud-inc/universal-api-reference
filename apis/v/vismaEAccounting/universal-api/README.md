# <img src="https://images.mindcloud.co/apps/icons/visma-eaccounting_1774297176089.png" alt="Visma eAccounting logo" width="28" height="28"> Visma eAccounting: Universal API

Manage customers, quotes, orders, and invoices in Visma eAccounting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vismaEAccounting/latest
- **Category:** Commerce / Accounting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eaccounting.vismaonline.com/
- **Vendor API docs:** https://eaccountingapi.vismaonline.com/scalar/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in Visma eAccounting. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from Visma eAccounting. |
| [List Articles](actions/list-articles.md) | GET | Retrieves all articles from Visma eAccounting. |
| [Replace Article](actions/replace-article.md) | PUT | Updates an existing article in Visma eAccounting. |

### Backorder

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Backorder](actions/create-order-backorder.md) | POST | Creates a backorder from an order in Visma eAccounting. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Visma eAccounting. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Visma eAccounting. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Visma eAccounting. |
| [List Customers](actions/list-customers.md) | GET | Retrieves all customers from Visma eAccounting. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Visma eAccounting. |

### Customer Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Invoice](actions/create-customer-invoice.md) | POST | Creates a new customer invoice in Visma eAccounting. |
| [Get Customer Invoice](actions/get-customer-invoice.md) | GET | Retrieves a customer invoice from Visma eAccounting. |
| [List Customer Invoices](actions/list-customer-invoices.md) | GET | Retrieves all customer invoices from Visma eAccounting. |
| [Send Customer Invoice Email](actions/send-customer-invoice-email.md) | POST | Sends a customer invoice email from Visma eAccounting. |
| [Void Customer Invoice](actions/void-customer-invoice.md) | PUT | Voids an existing customer invoice in Visma eAccounting. |

### Customer Invoice Draft

| Action | Method | Description |
| --- | --- | --- |
| [Convert Customer Invoice Draft To Customer Invoice](actions/convert-customer-invoice-draft-to-customer-invoice.md) | POST | Creates a customer invoice from a draft in Visma eAccounting. |
| [Create Customer Invoice Draft](actions/create-customer-invoice-draft.md) | POST | Creates a new customer invoice draft in Visma eAccounting. |
| [Delete Customer Invoice Draft](actions/delete-customer-invoice-draft.md) | DELETE | Deletes an existing customer invoice draft from Visma eAccounting. |
| [Get Customer Invoice Draft](actions/get-customer-invoice-draft.md) | GET | Retrieves a customer invoice draft from Visma eAccounting. |
| [List Customer Invoice Drafts](actions/list-customer-invoice-drafts.md) | GET | Retrieves all customer invoice drafts from Visma eAccounting. |
| [Replace Customer Invoice Draft](actions/replace-customer-invoice-draft.md) | PUT | Updates an existing customer invoice draft in Visma eAccounting. |

### Customer Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Invoice Payment](actions/create-customer-invoice-payment.md) | POST | Creates a customer invoice payment in Visma eAccounting. |

### Customer Invoice Payment Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Send Customer Invoice Payment Reminder](actions/send-customer-invoice-payment-reminder.md) | POST | Creates a payment reminder for a customer invoice in Visma eAccounting. |

### Customer Invoice Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Invoice PDF](actions/get-customer-invoice-pdf.md) | GET | Retrieves a customer invoice PDF from Visma eAccounting. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Complete Order](actions/complete-order.md) | PUT | Completes an existing order in Visma eAccounting. |
| [Convert Order To Customer Invoice](actions/convert-order-to-customer-invoice.md) | POST | Creates a customer invoice from an order in Visma eAccounting. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Visma eAccounting. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Visma eAccounting. |
| [List Orders](actions/list-orders.md) | GET | Retrieves all orders from Visma eAccounting. |
| [Send Order Email](actions/send-order-email.md) | POST | Sends an order email from Visma eAccounting. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Visma eAccounting. |

### Order Print

| Action | Method | Description |
| --- | --- | --- |
| [Print Order As PDF](actions/print-order-as-pdf.md) | GET | Retrieves an order PDF from Visma eAccounting. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Accept Quote](actions/accept-quote.md) | PUT | Accepts an existing quote in Visma eAccounting. |
| [Convert Quote To Customer Invoice](actions/convert-quote-to-customer-invoice.md) | POST | Creates a customer invoice from a quote in Visma eAccounting. |
| [Convert Quote To Order](actions/convert-quote-to-order.md) | POST | Creates an order from a quote in Visma eAccounting. |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in Visma eAccounting. |
| [Get Quote](actions/get-quote.md) | GET | Retrieves a quote from Visma eAccounting. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves all quotes from Visma eAccounting. |
| [Send Quote Email](actions/send-quote-email.md) | POST | Sends a quote email from Visma eAccounting. |
| [Update Quote](actions/update-quote.md) | PUT | Updates an existing quote in Visma eAccounting. |

