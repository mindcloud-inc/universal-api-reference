# Vtiger CRM: Native API Reference

A consolidated summary of Vtiger CRM's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://vtap.vtiger.com/platform/rest-apis.html
- **API base URL:** `{apiBaseUrl}`

## Authentication

### Vtiger Base64 Header Auth

Use the Vtiger API base URL plus the Base64 payload for username:accessKey. The action adds the Basic prefix.

### Credentials

- **API Base URL:** `apiBaseUrl` · required · Your Vtiger REST API base URL, for example https://your-company.od2.vtiger.com/restapi/v1/vtiger/default.
- **Authorization Header:** `authorizationHeader` · required · Base64 value of username:accessKey only. Do not include the Basic prefix.

[Official authentication documentation](https://help.vtiger.com/faq/162265706-What-username-and-password-should-I-use-when-calling-the-API-in-Postman)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /create?elementType=Accounts` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Contact](actions/create-contact.md) | `POST /create?elementType=Contacts` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Deal](actions/create-deal.md) | `POST /create?elementType=Potentials` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Invoice](actions/create-invoice.md) | `POST /create?elementType=Invoice` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Lead](actions/create-lead.md) | `POST /create?elementType=Leads` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Product](actions/create-product.md) | `POST /create?elementType=Products` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /create?elementType=PurchaseOrder` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Quote](actions/create-quote.md) | `POST /create?elementType=Quotes` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Record](actions/create-record.md) | `POST /create` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /create?elementType=SalesOrder` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Create Vendor](actions/create-vendor.md) | `POST /create?elementType=Vendors` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#create) |
| [Delete Record](actions/delete-record.md) | `POST /delete` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#delete) |
| [Describe Accounts](actions/describe-accounts.md) | `GET /describe?elementType=Accounts` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Contacts](actions/describe-contacts.md) | `GET /describe?elementType=Contacts` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Deals](actions/describe-deals.md) | `GET /describe?elementType=Potentials` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Invoices](actions/describe-invoices.md) | `GET /describe?elementType=Invoice` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Leads](actions/describe-leads.md) | `GET /describe?elementType=Leads` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Module](actions/describe-module.md) | `GET /describe` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Products](actions/describe-products.md) | `GET /describe?elementType=Products` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Purchase Orders](actions/describe-purchase-orders.md) | `GET /describe?elementType=PurchaseOrder` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Quotes](actions/describe-quotes.md) | `GET /describe?elementType=Quotes` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Sales Orders](actions/describe-sales-orders.md) | `GET /describe?elementType=SalesOrder` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Describe Vendors](actions/describe-vendors.md) | `GET /describe?elementType=Vendors` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#me---user-profile) |
| [List Accounts](actions/list-accounts.md) | `GET /query?query=select+id%2C+accountname+from+Accounts+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Contacts](actions/list-contacts.md) | `GET /query?query=select+id%2C+firstname%2C+lastname+from+Contacts+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Deals](actions/list-deals.md) | `GET /query?query=select+id%2C+potentialname+from+Potentials+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Invoices](actions/list-invoices.md) | `GET /query?query=select+id%2C+subject+from+Invoice+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Leads](actions/list-leads.md) | `GET /query?query=select+id%2C+firstname%2C+lastname+from+Leads+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Modules](actions/list-modules.md) | `GET /listtypes` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#listtypes---modules-list) |
| [List Products](actions/list-products.md) | `GET /query?query=select+id%2C+productname+from+Products+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /query?query=select+id%2C+subject+from+PurchaseOrder+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Quotes](actions/list-quotes.md) | `GET /query?query=select+id%2C+subject+from+Quotes+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /query?query=select+id%2C+subject+from+SalesOrder+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [List Vendors](actions/list-vendors.md) | `GET /query?query=select+id%2C+vendorname+from+Vendors+limit+0%2C+25%3B` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [Query Records](actions/query-records.md) | `GET /query` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#query) |
| [Retrieve Record](actions/retrieve-record.md) | `GET /retrieve` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#retrieve) |
| [Revise Record](actions/revise-record.md) | `POST /revise` | [docs](https://vtap.vtiger.com/platform/rest-apis.html#revise) |
