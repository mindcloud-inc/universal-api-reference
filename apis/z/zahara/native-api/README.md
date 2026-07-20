# Zahara: Native API Reference

A consolidated summary of Zahara's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://ask.zaharasoftware.com/api-docs
- **API base URL:** `https://api.myzahara.net`

## Authentication

### Zahara API Keys

Use the tenancy API key, business unit API key, and tenancy ID from Zahara.

### Credentials

- **Tenancy API Key:** `tenancyApiKey` · required · API key from Zahara Admin > Settings > Integrations for tenancy-level endpoints.
- **Business Unit API Key:** `businessUnitApiKey` · required · Business unit API key returned from the Zahara BusinessUnit endpoint for business-unit endpoints.
- **Tenancy ID:** `tenancyId` · required · Tenancy identifier used for Zahara reporting and premium data workflows.

[Official authentication documentation](https://ask.zaharasoftware.com/api/articles/article/reporting-api?type=1)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | `POST /api/{{credentials.businessUnitApiKey}}/Invoice/Add` | [docs](https://ask.zaharasoftware.com/api-docs/add-invoice) |
| [Create Project](actions/create-project.md) | `POST /api/{{credentials.businessUnitApiKey}}/Project/Add` | [docs](https://ask.zaharasoftware.com/api-docs/add-project) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Add` | [docs](https://ask.zaharasoftware.com/api-docs/add-purchase-order) |
| [Create Supplier](actions/create-supplier.md) | `POST /api/{{credentials.businessUnitApiKey}}/Supplier/Add` | [docs](https://ask.zaharasoftware.com/api-docs/add-supplier) |
| [Get Invoice By ID](actions/get-invoice-by-id.md) | `GET /api/{{credentials.businessUnitApiKey}}/Invoice/Get/{{documentId}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-invoices-by-id) |
| [Get Project By ID](actions/get-project-by-id.md) | `GET /api/{{credentials.businessUnitApiKey}}/Project/Get/{{projectId}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-project-by-id) |
| [Get Purchase Order By ID](actions/get-purchase-order-by-id.md) | `GET /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Get/{{documentId}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-purchase-order-by-id) |
| [Get Supplier By ID](actions/get-supplier-by-id.md) | `GET /api/{{credentials.businessUnitApiKey}}/Supplier/Get/{{supplierId}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-supplier-by-id) |
| [List Business Units](actions/list-business-units.md) | `GET /api/{{credentials.tenancyApiKey}}/BusinessUnit/GetAll` | [docs](https://ask.zaharasoftware.com/api-docs/get-business-units) |
| [List Currencies](actions/list-currencies.md) | `GET /api/{{credentials.tenancyApiKey}}/Currencies` | [docs](https://ask.zaharasoftware.com/api-docs/currencies) |
| [List Invoices After Date](actions/list-invoices-after-date.md) | `GET /api/{{credentials.businessUnitApiKey}}/Invoice/After/{{date}}/{{skip}}/{{take}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-invoices-after-date-with-skip-and-take) |
| [List Projects](actions/list-projects.md) | `GET /api/{{credentials.businessUnitApiKey}}/Project/GetAll` | [docs](https://ask.zaharasoftware.com/api-docs/get-all-projects) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Get/{{skip}}/{{take}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-all-purchase-orders) |
| [List Purchase Orders After Date](actions/list-purchase-orders-after-date.md) | `GET /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/After/{{date}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-orders-after-date) |
| [List Suppliers After Date](actions/list-suppliers-after-date.md) | `GET /api/{{credentials.businessUnitApiKey}}/Supplier/After/{{date}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-suppliers-after-date) |
| [List Users (Business Unit)](actions/list-users-business-unit.md) | `GET /api/{{credentials.businessUnitApiKey}}/User/GetAll` | [docs](https://ask.zaharasoftware.com/api-docs/get-all-users) |
| [List Users (Tenancy)](actions/list-users-tenancy.md) | `GET /api/{{credentials.tenancyApiKey}}/User/GetAll` | [docs](https://ask.zaharasoftware.com/api-docs/get-all-users) |
| [List Workflows](actions/list-workflows.md) | `GET /api/{{credentials.businessUnitApiKey}}/Process/GetAll` | [docs](https://ask.zaharasoftware.com/api-docs/get-all-workflows) |
| [Search Suppliers](actions/search-suppliers.md) | `GET /api/{{credentials.businessUnitApiKey}}/Supplier/Search/{{searchTerm}}` | [docs](https://ask.zaharasoftware.com/api-docs/get-suppliers-by-search) |
| [Update Invoice](actions/update-invoice.md) | `PUT /api/{{credentials.businessUnitApiKey}}/Invoice/Update/{{documentId}}` | [docs](https://ask.zaharasoftware.com/api-docs/update-invoice) |
| [Update Project](actions/update-project.md) | `PUT /api/{{credentials.businessUnitApiKey}}/Project/Update/{{projectId}}` | [docs](https://ask.zaharasoftware.com/api-docs/update-project) |
| [Update Purchase Order](actions/update-purchase-order.md) | `PUT /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Update/{{documentId}}` | [docs](https://ask.zaharasoftware.com/api-docs/update-purchase-order) |
| [Update Supplier](actions/update-supplier.md) | `PUT /api/{{credentials.businessUnitApiKey}}/Supplier/Update/{{supplierId}}` | [docs](https://ask.zaharasoftware.com/api-docs/update-supplier) |
| [Upload Invoice PDF](actions/upload-invoice-pdf.md) | `POST /api/{{credentials.businessUnitApiKey}}/Invoice/Upload/{{documentId}}` | [docs](https://ask.zaharasoftware.com/api-docs/upload-invoice-pdf) |
