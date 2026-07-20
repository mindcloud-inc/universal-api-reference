# Kiwili: Native API Reference

A consolidated summary of Kiwili's API configuration and 54 documented operations, with links to official documentation.

- **Official docs:** https://api.kiwili.com/api/openapi/
- **API base URL:** `https://mindcloud.kiwili.com/api`

## Authentication

### API Key

Use your Kiwili API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (54 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact` | [docs](https://api.kiwili.com/api/openapi/) |
| [Create Enterprise](actions/create-enterprise.md) | `POST /enterprise` | [docs](https://api.kiwili.com/api/openapi/) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://api.kiwili.com/api/openapi/) |
| [Create Project](actions/create-project.md) | `POST /project` | [docs](https://api.kiwili.com/api/openapi/) |
| [Create Service](actions/create-service.md) | `POST /service` | [docs](https://api.kiwili.com/api/openapi/) |
| [Create Task](actions/create-task.md) | `POST /task` | [docs](https://api.kiwili.com/api/openapi/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:contact_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Delete Enterprise](actions/delete-enterprise.md) | `DELETE /enterprise/:enterprise_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Delete Product](actions/delete-product.md) | `DELETE /product/:product_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Delete Service](actions/delete-service.md) | `DELETE /service/:service_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Accounting Code Details](actions/get-accounting-code-details.md) | `GET /accountingcode/:accounting_code_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Bank Account Details](actions/get-bank-account-details.md) | `GET /bankaccount/:bank_account_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Company Details](actions/get-company-details.md) | `GET /company/:company_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Contact Details](actions/get-contact-details.md) | `GET /contact/:contact_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Currency Details](actions/get-currency-details.md) | `GET /currency/:currency_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Enterprise Details](actions/get-enterprise-details.md) | `GET /enterprise/:enterprise_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Estimate Details](actions/get-estimate-details.md) | `GET /estimate/:estimate_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Expense Details](actions/get-expense-details.md) | `GET /expense/:expense_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Invoice Details](actions/get-invoice-details.md) | `GET /invoice/:invoice_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Invoice Payment Details](actions/get-invoice-payment-details.md) | `GET /invoicepayment/:invoice_payment_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Payment Type Details](actions/get-payment-type-details.md) | `GET /paymenttype/:payment_type_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Product Details](actions/get-product-details.md) | `GET /product/:product_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Project Details](actions/get-project-details.md) | `GET /project/:project_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Purchase Order Details](actions/get-purchase-order-details.md) | `GET /purchaseorder/:purchase_order_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Service Details](actions/get-service-details.md) | `GET /service/:service_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Task Details](actions/get-task-details.md) | `GET /task/:task_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Tax Profile Details](actions/get-tax-profile-details.md) | `GET /taxprofile/:tax_profile_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get Time Entry Details](actions/get-time-entry-details.md) | `GET /timeentry/:time_entry_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Get User Details](actions/get-user-details.md) | `GET /user/:user_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Accounting Codes](actions/list-accounting-codes.md) | `GET /accountingcode` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bankaccount` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Companies](actions/list-companies.md) | `GET /company` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Contacts](actions/list-contacts.md) | `GET /contact` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Currencies](actions/list-currencies.md) | `GET /currency` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Enterprises](actions/list-enterprises.md) | `GET /enterprise` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Estimates](actions/list-estimates.md) | `GET /estimate` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Expenses](actions/list-expenses.md) | `GET /expense` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Invoice Payments](actions/list-invoice-payments.md) | `GET /invoicepayment` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Payment Types](actions/list-payment-types.md) | `GET /paymenttype` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchaseorder` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Services](actions/list-services.md) | `GET /service` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Tasks](actions/list-tasks.md) | `GET /task` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Tax Profiles](actions/list-tax-profiles.md) | `GET /taxprofile` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Time Entries](actions/list-time-entries.md) | `GET /timeentry` | [docs](https://api.kiwili.com/api/openapi/) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:contact_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Enterprise](actions/update-enterprise.md) | `PUT /enterprise/:enterprise_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Product](actions/update-product.md) | `PUT /product/:product_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Project](actions/update-project.md) | `PUT /project/:project_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Service](actions/update-service.md) | `PUT /service/:service_id` | [docs](https://api.kiwili.com/api/openapi/) |
| [Update Task](actions/update-task.md) | `PUT /task/:task_id` | [docs](https://api.kiwili.com/api/openapi/) |
