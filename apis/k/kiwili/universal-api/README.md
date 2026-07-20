# <img src="https://images.mindcloud.co/apps/icons/kiwili_1774874785722.png" alt="Kiwili logo" width="28" height="28"> Kiwili: Universal API

Kiwili is an ERP and business management platform for small businesses, covering enterprises, contacts, invoices, expenses, projects, time, products, services, and related finance operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kiwili/latest
- **Actions:** 54
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kiwili.com
- **Vendor API docs:** https://api.kiwili.com/api/openapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Enterprises](actions/list-enterprises.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/list-enterprises?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (54)

### Accounting Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounting Code Details](actions/get-accounting-code-details.md) | GET | Retrieves details for an accounting code in Kiwili. |
| [List Accounting Codes](actions/list-accounting-codes.md) | GET | Retrieves all accounting codes from Kiwili. |

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Bank Account Details](actions/get-bank-account-details.md) | GET | Retrieves details for a bank account in Kiwili. |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves all bank accounts from Kiwili. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | GET | Retrieves details for a company in Kiwili. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all company records from Kiwili. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Kiwili. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Kiwili. |
| [Get Contact Details](actions/get-contact-details.md) | GET | Retrieves details for a contact in Kiwili. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contact records from Kiwili. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Kiwili. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency Details](actions/get-currency-details.md) | GET | Retrieves details for a currency in Kiwili. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves all currency records from Kiwili. |

### Enterprise

| Action | Method | Description |
| --- | --- | --- |
| [Create Enterprise](actions/create-enterprise.md) | POST | Creates a new enterprise in Kiwili. |
| [Delete Enterprise](actions/delete-enterprise.md) | DELETE | Deletes an existing enterprise from Kiwili. |
| [Get Enterprise Details](actions/get-enterprise-details.md) | GET | Retrieves details for an enterprise in Kiwili. |
| [List Enterprises](actions/list-enterprises.md) | GET | Retrieves all enterprise records from Kiwili. |
| [Update Enterprise](actions/update-enterprise.md) | PUT | Updates an existing enterprise in Kiwili. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Estimate Details](actions/get-estimate-details.md) | GET | Retrieves details for an estimate in Kiwili. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves all estimate records from Kiwili. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Get Expense Details](actions/get-expense-details.md) | GET | Retrieves details for an expense in Kiwili. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves all expense records from Kiwili. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Details](actions/get-invoice-details.md) | GET | Retrieves details for an invoice in Kiwili. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves all invoice records from Kiwili. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Payment Details](actions/get-invoice-payment-details.md) | GET | Retrieves details for an invoice payment in Kiwili. |
| [List Invoice Payments](actions/list-invoice-payments.md) | GET | Retrieves all invoice payments from Kiwili. |

### Payment Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Type Details](actions/get-payment-type-details.md) | GET | Retrieves details for a payment type in Kiwili. |
| [List Payment Types](actions/list-payment-types.md) | GET | Retrieves all payment types from Kiwili. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Kiwili. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Kiwili. |
| [Get Product Details](actions/get-product-details.md) | GET | Retrieves details for a product in Kiwili. |
| [List Products](actions/list-products.md) | GET | Retrieves all product records from Kiwili. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Kiwili. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Kiwili. |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves details for a project in Kiwili. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Kiwili. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Kiwili. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order Details](actions/get-purchase-order-details.md) | GET | Retrieves details for a purchase order in Kiwili. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves all purchase orders from Kiwili. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in Kiwili. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes an existing service from Kiwili. |
| [Get Service Details](actions/get-service-details.md) | GET | Retrieves details for a service in Kiwili. |
| [List Services](actions/list-services.md) | GET | Retrieves all service records from Kiwili. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in Kiwili. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Kiwili. |
| [Get Task Details](actions/get-task-details.md) | GET | Retrieves details for a task in Kiwili. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from Kiwili. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Kiwili. |

### Tax Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Profile Details](actions/get-tax-profile-details.md) | GET | Retrieves details for a tax profile in Kiwili. |
| [List Tax Profiles](actions/list-tax-profiles.md) | GET | Retrieves all tax profiles from Kiwili. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entry Details](actions/get-time-entry-details.md) | GET | Retrieves details for a time entry in Kiwili. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves all time entries from Kiwili. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves details for a user in Kiwili. |
| [List Users](actions/list-users.md) | GET | Retrieves all user records from Kiwili. |

