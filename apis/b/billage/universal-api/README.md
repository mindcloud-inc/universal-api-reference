# <img src="https://images.mindcloud.co/apps/icons/billage_1774547296460.png" alt="Billage logo" width="28" height="28"> Billage: Universal API

Manage contacts, invoices, budgets, products, and spendings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billage/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getbillage.com
- **Vendor API docs:** https://app.getbillage.com/api/documentation.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billage/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Billage. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account record from Billage. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves account records from Billage by criteria. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Billage. |

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [Create Budget](actions/create-budget.md) | POST | Creates a new budget in Billage. |
| [Get Budget](actions/get-budget.md) | GET | Retrieves a budget record from Billage. |
| [List Budgets](actions/list-budgets.md) | GET | Retrieves budget records from Billage by code or date. |
| [Update Budget](actions/update-budget.md) | PUT | Updates an existing budget in Billage. |

### Company Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info.md) | GET | Retrieves company profile information from Billage. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Billage. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from Billage. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from Billage by criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Billage. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Billage. |
| [Get Invoice by Reference](actions/get-invoice-by-reference.md) | GET | Retrieves an invoice from Billage by reference code. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoice records from Billage by code or date. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Billage. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Billage. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Billage by alias or name. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Billage. |

### Spending

| Action | Method | Description |
| --- | --- | --- |
| [Create Spending](actions/create-spending.md) | POST | Creates a new spending in Billage. |
| [Get Spending by Reference](actions/get-spending-by-reference.md) | GET | Retrieves a spending from Billage by reference code. |
| [List Spendings](actions/list-spendings.md) | GET | Retrieves spending records from Billage by code or date. |
| [Update Spending](actions/update-spending.md) | PUT | Updates an existing spending in Billage. |

