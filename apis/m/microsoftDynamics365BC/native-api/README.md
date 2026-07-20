# Microsoft Dynamics 365 BC: Native API Reference

A consolidated summary of Microsoft Dynamics 365 BC's API configuration and 50 documented operations.

- **REST base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **REST (Copy) base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`

## Authentication

### OAuth 2.0

### Credentials

- **Tenant Id:** `tenantId` · optional
- **Environment:** `environment` · optional
- **Client Id:** `clientId` · optional
- **Client Secret:** `clientSecret` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://api.businesscentral.dynamics.com/.default offline_access`.

Refresh expired access tokens with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow#request-an-authorization-code)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `value`.

### REST (Copy)

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `value`.

## Pagination

- **REST:** Use `$top` in the query string to set the page size (default 100; accepted range 1–20000). Use `$skip` in the query string to choose the result range.
- **REST (Copy):** Use `$top` in the query string to set the page size (default 100; accepted range 1–20000). Use `$skip` in the query string as the record offset.

## Endpoints (50 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Create Bank Deposit Lines ODataV4](actions/create-bank-deposit-lines-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudBankDepositLines` |  |
| [Create Bank Deposit ODataV4](actions/create-bank-deposit-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudBankDepositHeader` |  |
| [Create Costumer ODataV4](actions/create-costumer-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:companyId)/MindcloudCustomerCard` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_update) |
| [Create Credit Memo](actions/create-credit-memo.md) | REST | `POST v2.0/companies(:company_id)/salesCreditMemos` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create) |
| [Create Credit Memo Itens ODataV4](actions/create-credit-memo-itens-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudCreditMemoSalesLines` |  |
| [Create Credit Memo Line Item](actions/create-credit-memo-line-item.md) | REST | `POST v2.0/companies(:company_id)/salesCreditMemos(:creditMemoId)/salesCreditMemoLines` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create) |
| [Create Customer](actions/create-customer.md) | REST | `POST v2.0/companies(:company_id)/customers` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create) |
| [Create Customer SSI](actions/create-customer-ssi.md) | REST (Copy) | `POST v2.0/companies(:company_id)/customersSSI` | [docs](https://anotepad.com/notes/nih23qmd) |
| [Create General Journal ODataV4](actions/create-general-journal-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudGeneralJournal` |  |
| [Create Journal Line ODataV4](actions/create-journal-line-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/Cash_Receipt_Journals_Excel` |  |
| [Create Project Job Planning Lines ODataV4](actions/create-project-job-planning-lines-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/Job_Planning_Lines` |  |
| [Create Project Job Task Lines ODataV4](actions/create-project-job-task-lines-o-data-v4.md) | REST | `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/Job_Task_Lines` |  |
| [Create Sales Invoice Line Item](actions/create-sales-invoice-line-item.md) | REST | `POST v2.0/companies({{companyId}})/salesInvoices(:invoiceId)/salesInvoiceLines` |  |
| [Create Sales Invoices](actions/create-sales-invoices.md) | REST | `POST v2.0/companies({{companyId}})/salesInvoices` |  |
| [Create Sales Order](actions/create-sales-order.md) | REST | `POST companies(:id)/salesOrders` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_create) |
| [Create Sales Order Line](actions/create-sales-orders-lines.md) | REST | `POST v2.0/companies(:companyId)/salesOrders(:salesOrderId)/salesOrderLines` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorderline_create) |
| [Create Ship-to Addresses SSI](actions/create-ship-to-addresses-ssi.md) | REST (Copy) | `POST v2.0/companies(:company_id)/shipToAddressesSSI` | [docs](https://anotepad.com/notes/x8dnaab8) |
| [Delete Sales Invoice Line Item](actions/delete-sales-invoice-line-item.md) | REST | `DELETE v2.0/companies(:companyId)/salesInvoices(:salesInvoiceId)/salesInvoiceLines(:lineItemId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [Get Inventory By Location SSI](actions/get-inventory-by-location-ssi.md) | REST (Copy) | `GET v2.0/companies(:company_id)/inventoryQtyByLocationsSSI` | [docs](https://anotepad.com/notes/x8dnaab8) |
| [Get Ship-to Addresses SSI](actions/get-ship-to-addresses-ssi.md) | REST (Copy) | `GET v2.0/companies(:company_id)/shipToAddressesSSI` | [docs](https://anotepad.com/notes/x8dnaab8) |
| [List Bank Deposits Line ODataV4](actions/list-bank-deposits-line-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudBankDepositLines` |  |
| [List Bank Deposits ODataV4](actions/list-bank-deposits-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudBankDepositHeader` |  |
| [List Companies](actions/list-companies.md) | REST | `GET v2.0/companies` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_company_get) |
| [List Credit Memo ODataV4](actions/list-credit-memo-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudCreditMemo` |  |
| [List Customers](actions/list-customers.md) | REST (Copy) | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/v2.0/companies({{companyId}})/customers` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List Customers ODataV4](actions/list-customers-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudCustomerCard` |  |
| [List Customers SSI](actions/list-customers-ssi.md) | REST (Copy) | `GET v2.0/companies({{companyId}})/CustomersSSI` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List Employees ODataV4](actions/list-employees-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:companyId)/GravityResources` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List General Journal ODataV4](actions/list-general-journal-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudGeneralJournal` |  |
| [List Items](actions/list-items.md) | REST | `GET v2.0/companies({{companyId}})/items` |  |
| [List Journal Line](actions/list-journal-line.md) | REST | `GET v2.0/companies(:company_id)/journals(:journal_id)/journalLines` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_get) |
| [List Journal Lines Payments ODataV4](actions/list-journal-lines-payments-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/Cash_Receipt_Journals_Excel` |  |
| [List Payroll Journal ODataV4](actions/list-payroll-journal-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudPayrollJournal` |  |
| [List Projects](actions/list-projects.md) | REST | `GET v2.0/companies({{companyId}})/projects` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List Sales Invoice](actions/list-sales-invoice.md) | REST | `GET v2.0/companies(:companyId)/salesInvoices` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List Sales Invoice Line Items](actions/list-sales-invoice-line-items.md) | REST | `GET v2.0/companies({{companyId}})/salesInvoices(:salesInvoiceId)/salesInvoiceLines` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [List Sales Invoice ODataV4](actions/list-sales-invoice-o-data-v4.md) | REST | `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudSalesInvoice` |  |
| [List Sales Orders Lines SSI](actions/list-sales-orders-lines-ssi.md) | REST (Copy) | `GET v2.0/companies(:company_id)/salesLinesSSI` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_get) |
| [List Sales Orders SSI](actions/list-sales-orders-ssi.md) | REST (Copy) | `GET v2.0/companies(:company_id)/salesHeadersSSI(:id)` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_get) |
| [Post Credit Memo](actions/post-credit-memo.md) | REST | `POST v2.0/companies({{companyId}})/salesCreditMemos({{creditMemoId}})/Microsoft.NAV.post` |  |
| [Post Journal Lines](actions/post-journal-lines.md) | REST | `POST v2.0/companies({{companyId}})/journals({{journalId}})/Microsoft.NAV.post` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [Post Sales Invoice](actions/post-sales-invoice.md) | REST | `POST v2.0/companies({{companyId}})/salesInvoices({{invoiceId}})/Microsoft.NAV.post` |  |
| [Update Costumer ODataV4](actions/update-costumer-o-data-v4.md) | REST | `PATCH https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:companyId)/MindcloudCustomerCard(':customerId')` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_update) |
| [Update Costumer SSI](actions/update-costumer-ssi.md) | REST (Copy) | `PATCH v2.0/companies(:companyId)/customersSSI(:customerId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_update) |
| [Update Customer Payment ODataV4](actions/update-customer-payment-o-data-v4.md) | REST | `PATCH https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/Cash_Receipt_Journals_Excel(Journal_Template_Name=':journalTemplateName',Journal_Batch_Name=':journalBatchName',Line_No=:lineNo)` |  |
| [Update Dimension](actions/update-dimension.md) | REST | `PATCH v2.0/companies({{companyId}})/dimensionValues({{dimensionId}})` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get) |
| [Update Project](actions/update-project.md) | REST | `PATCH v2.0/companies({{companyId}})/projects(:projectId)` |  |
| [Update Sales Order SSI](actions/update-sales-order-ssi.md) | REST (Copy) | `PATCH /v2.0/companies(:id)/salesHeadersSSI(:salesOrderID)` | [docs](https://anotepad.com/notes/ccfg4kec) |
| [Update Sales Orders Lines](actions/update-sales-orders-lines.md) | REST | `PATCH v2.0/companies(:companyId)/salesOrders(:salesOrderId)/salesOrderLines(:salesOrderLineId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorderline_create) |
| [Update Ship-to Addresses SSI](actions/update-ship-to-addresses-ssi.md) | REST (Copy) | `PATCH v2.0/companies(:company_id)/shipToAddressesSSI(CustomerNo=':customerNo',Code=':shipToAddressCode')` | [docs](https://anotepad.com/notes/x8dnaab8) |
