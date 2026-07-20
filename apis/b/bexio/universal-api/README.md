# <img src="https://images.mindcloud.co/apps/icons/bexio_1773341910490.png" alt="Bexio logo" width="28" height="28"> Bexio: Universal API

Manage contacts, quotes, invoices, and accounting in Bexio

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bexio/latest
- **Category:** Commerce / ERP
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bexio.com/
- **Vendor API docs:** https://docs.bexio.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [List Bills](actions/list-bills.md) | GET | Retrieves bills from Bexio. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Bexio. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Bexio. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Bexio. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Bexio by search criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Bexio. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates an expense in Bexio. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from Bexio. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from Bexio. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in Bexio. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Bexio. |
| [Issue Invoice](actions/issue-invoice.md) | PUT | Issues an invoice in Bexio. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Bexio. |
| [Send Invoice](actions/send-invoice.md) | PUT | Sends an invoice from Bexio by email. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice Payment](actions/create-invoice-payment.md) | POST | Creates an invoice payment in Bexio. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a quote in Bexio. |
| [Get Quote](actions/get-quote.md) | GET | Retrieves a quote from Bexio. |
| [Issue Quote](actions/issue-quote.md) | PUT | Issues a quote in Bexio. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves quotes from Bexio. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a purchase order in Bexio. |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from Bexio. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Bexio. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Bexio. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Bexio. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Bexio. |

