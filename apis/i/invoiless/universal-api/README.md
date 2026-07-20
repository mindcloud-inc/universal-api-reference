# <img src="https://images.mindcloud.co/apps/icons/invoiless-icon_1776973310274.png" alt="Invoiless logo" width="28" height="28"> Invoiless: Universal API

Create, send, and manage invoices and customers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invoiless/latest
- **Category:** Commerce / Accounting
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://invoiless.com
- **Vendor API docs:** https://docs.invoiless.com/guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Invoices](actions/list-invoices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Invoiless. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Invoiless. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Invoiless. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Invoiless. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Invoiless. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Invoiless. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Invoiless. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Invoiless. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Invoiless. |
| [Send Invoice](actions/send-invoice.md) | PUT | Sends an invoice to a customer in Invoiless. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Invoiless. |

