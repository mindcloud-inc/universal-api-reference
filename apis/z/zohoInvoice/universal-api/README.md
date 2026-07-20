# <img src="https://images.mindcloud.co/apps/icons/608f5d206e590b696d06e2e54409efe1_1775228350649.png" alt="Zoho Invoice logo" width="28" height="28"> Zoho Invoice: Universal API

Create invoices, track expenses, and manage projects and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoInvoice/latest
- **Category:** Commerce / Accounting
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/invoice/
- **Vendor API docs:** https://www.zoho.com/invoice/api/v3/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Zoho Invoice. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Zoho Invoice. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Zoho Invoice. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Zoho Invoice. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates an estimate in Zoho Invoice. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from Zoho Invoice. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from Zoho Invoice. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an estimate in Zoho Invoice. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates an expense in Zoho Invoice. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from Zoho Invoice. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from Zoho Invoice. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an expense in Zoho Invoice. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in Zoho Invoice. |
| [Email Invoice](actions/email-invoice.md) | POST | Emails an invoice from Zoho Invoice. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Zoho Invoice. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Zoho Invoice. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in Zoho Invoice. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates an item in Zoho Invoice. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Zoho Invoice. |
| [List Items](actions/list-items.md) | GET | Retrieves items from Zoho Invoice. |
| [Update Item](actions/update-item.md) | PUT | Updates an item in Zoho Invoice. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Zoho Invoice. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a payment in Zoho Invoice. |
| [List Customer Payments](actions/list-customer-payments.md) | GET | Retrieves customer payments from Zoho Invoice. |
| [Retrieve Payment](actions/retrieve-payment.md) | GET | Retrieves a payment from Zoho Invoice. |

