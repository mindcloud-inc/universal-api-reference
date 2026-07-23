# Rillion Prime: Native API Reference

A consolidated summary of Rillion Prime's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://rillion-prime-integration.readme.io/docs/using-the-api-reference
- **API base URL:** `{baseUrl}`

## Authentication

### Custom

### Credentials

- **Client ID:** `clientId` · required · OAuth client ID for the selected Rillion Prime environment.
- **Client secret:** `clientSecret` · required · OAuth client secret for the selected Rillion Prime environment.
- **Environment:** `baseUrl` · required · Enter the full Rillion Prime API host for the environment you want to use. Example: https://prime-2-uat-14-ue.rillionprime.com/api/v1.0
- **Identity Server URL:** `authServer` · required · Enter the tenant-specific IdentityServer base URL for this environment. Example: https://tenant.rillionprime.com/identityserver
- **Tenant ID:** `tenantId` · required
- **User:** `user` · required · User sent in the Prime /Authorize exchange. Example: AdminUser
- **Role:** `role` · required · Role sent in the Prime /Authorize exchange. Example: Administrator

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://rillion-prime-integration.readme.io/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `PageSize` in the query string to set the page size. Use `PageIndex` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Purchase Order Delivery Queue Records](actions/create-purchase-order-delivery-queue-records.md) | `PUT /purchaseorderdeliveryqueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Buyer%20-%20v1.0) |
| [Get Invoice Details](actions/get-invoice-details.md) | `GET /invoice/detail` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [Get Invoice Log Table Metadata](actions/get-invoice-log-table-metadata.md) | `GET /invoicequeue/metadata/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [Get Invoice Queue](actions/get-invoice-queue.md) | `GET /invoicequeue/:invoiceQueueId/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [Get Language](actions/get-language.md) | `GET /language/:LanguageID` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=System%20-%20v1.0) |
| [Get User Preferences](actions/get-user-preferences.md) | `GET /preferences` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Accounts By Role](actions/list-accounts-by-role.md) | `GET /account/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Allocation Types For Role](actions/list-allocation-types-for-role.md) | `GET /allocationType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Asset Types For Role](actions/list-asset-types-for-role.md) | `GET /assettype/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Companies By Role](actions/list-companies-by-role.md) | `GET /company/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Currencies](actions/list-currencies.md) | `GET /currency` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Flow Proposal For Role](actions/list-flow-proposal-for-role.md) | `GET /invoice/FlowProposal/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [List Group Types](actions/list-group-types.md) | `GET /groupType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=System%20-%20v1.0) |
| [List Invoice Queue](actions/list-invoice-queue.md) | `GET /invoicequeue/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [List Languages](actions/list-languages.md) | `GET /language` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=System%20-%20v1.0) |
| [List Object Relation](actions/list-object-relation.md) | `GET /objectRelation` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Object Relation Setting](actions/list-object-relation-setting.md) | `GET /objectRelationSetting` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Object Types](actions/list-object-types.md) | `GET /objectType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=System%20-%20v1.0) |
| [List Objects For Role](actions/list-objects-for-role.md) | `GET /object/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Payment Approvals](actions/list-payment-approvals.md) | `GET /payment/approval` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | `GET /payment/configuration/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Permissions](actions/list-payment-permissions.md) | `GET /payment/permission` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Schedules](actions/list-payment-schedules.md) | `GET /payment/schedule` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Statuses](actions/list-payment-statuses.md) | `GET /payment/status` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Supplier Statuses](actions/list-payment-supplier-statuses.md) | `GET /payment/supplier/status` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Suppliers](actions/list-payment-suppliers.md) | `GET /payment/supplier` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Tenant Company Configurations](actions/list-payment-tenant-company-configurations.md) | `GET /payment/configuration/tenant/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Tenant Configurations](actions/list-payment-tenant-configurations.md) | `GET /payment/configuration/tenant` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Tenant Provider Configurations](actions/list-payment-tenant-provider-configurations.md) | `GET /payment/configuration/tenant/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payments](actions/list-payments.md) | `GET /payment` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Pending Supplier Payments](actions/list-pending-supplier-payments.md) | `GET /payment/supplier/payments/pending` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Periods For Role](actions/list-periods-for-role.md) | `GET /period/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List Purchase Order Deliveries For Import In Queue](actions/list-purchase-order-deliveries-for-import-in-queue.md) | `POST /purchaseorderdeliveryqueue/ListPurchaseOrderDeliveryForImportInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Buyer%20-%20v1.0) |
| [List Role Operation Permissions](actions/list-role-operation-permissions.md) | `GET /role/operationpermissiongroup` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Role%20-%20v1.0) |
| [List Roles](actions/list-roles.md) | `GET /role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Role%20-%20v1.0) |
| [List Suppliers For Role](actions/list-suppliers-for-role.md) | `GET /supplier/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [List VAT Codes For Role](actions/list-vat-codes-for-role.md) | `GET /vatcode/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0) |
| [Search For Expenditures](actions/search-for-expenditures.md) | `GET /budget/search/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0) |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | `GET /payment/supplier/typeahead` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
