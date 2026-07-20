# Rillion Prime: Native API Reference

A consolidated summary of Rillion Prime's API configuration and 140 documented operations, with links to official documentation.

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

## Endpoints (140 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Invoice Receipt To Invoice Queue](actions/add-invoice-receipt-to-invoice-queue.md) | `PUT /invoicequeue/receipt` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Approve Invoice For Role](actions/approve-invoice-for-role.md) | `POST /invoice/approve/:invoiceId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Approve Invoices For Roles](actions/approve-invoices-for-roles.md) | `POST /invoice/approve` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Approve Payments](actions/approve-payments.md) | `POST /payment/process/approve` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Auto Match Invoices](actions/auto-match-invoices.md) | `POST /invoice/match` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Calculate Vat Account Coding For Invoice](actions/calculate-vat-account-coding-for-invoice.md) | `POST /invoice/:invoiceId/CalculateVat/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Cancel Invoice For Role](actions/cancel-invoice-for-role.md) | `POST /invoice/cancel/:invoiceId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Cancel Payments](actions/cancel-payments.md) | `POST /payment/process/cancel` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Change Invoice Payment Dates By Company Supplier And Invoice Number](actions/change-invoice-payment-dates-by-company-supplier-and-invoice-number.md) | `PUT /invoice/changeinvoicepaymentdatebyuq` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Change Invoice Payment Dates By Series And Number](actions/change-invoice-payment-dates-by-series-and-number.md) | `PUT /invoice/changeinvoicepaymentdate` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Change Invoice Queue Account Coding Date](actions/change-invoice-queue-account-coding-date.md) | `POST /invoicequeue/changeaccountcodingdate` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Copy Invoice Diary Attachments](actions/copy-invoice-diary-attachments.md) | `POST /CopyInvoiceDiaryAttachments` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Account](actions/create-account.md) | `PUT /account` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Asset](actions/create-asset.md) | `PUT /asset` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Asset Type](actions/create-asset-type.md) | `PUT /assettype` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Code Relation](actions/create-code-relation.md) | `PUT /coderelation` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Commodity](actions/create-commodity.md) | `PUT /commodity` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Company](actions/create-company.md) | `PUT /company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Currency](actions/create-currency.md) | `PUT /currency` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Holiday](actions/create-holiday.md) | `PUT /holiday` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Invoice Diary Post](actions/create-invoice-diary-post.md) | `POST /invoice/diary` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Invoice Diary Post By Invoice](actions/create-invoice-diary-post-by-invoice.md) | `POST /invoice/:invoiceId/diary` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Invoice Queue](actions/create-invoice-queue.md) | `POST /invoicequeue/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Licences](actions/create-licences.md) | `POST /licence` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Locked Rows](actions/create-locked-rows.md) | `POST /lockedRow` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Object](actions/create-object.md) | `PUT /object` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Object Type](actions/create-object-type.md) | `PUT /objecttype` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Approval](actions/create-payment-approval.md) | `POST /payment/approval` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Configuration Company](actions/create-payment-configuration-company.md) | `POST /payment/configuration/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Creation Trigger](actions/create-payment-creation-trigger.md) | `POST /payment/creation/trigger` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Export Job](actions/create-payment-export-job.md) | `POST /payment/export` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Schedule](actions/create-payment-schedule.md) | `POST /payment/schedule` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Supplier Grouping](actions/create-payment-supplier-grouping.md) | `POST /payment/suppliers/grouping` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Tenant Company Configuration](actions/create-payment-tenant-company-configuration.md) | `POST /payment/configuration/tenant/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Tenant Configuration](actions/create-payment-tenant-configuration.md) | `POST /payment/configuration/tenant` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Payment Tenant Provider Configuration](actions/create-payment-tenant-provider-configuration.md) | `POST /payment/configuration/tenant/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Period Queue Record](actions/create-period-queue-record.md) | `PUT /period` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Purchase Order Delivery Queue Records](actions/create-purchase-order-delivery-queue-records.md) | `PUT /purchaseorderdeliveryqueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Purchase Order Queue Records](actions/create-purchase-order-queue-records.md) | `PUT /purchaseorderqueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Supplier](actions/create-supplier.md) | `PUT /supplier` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create Supplier Bank Account](actions/create-supplier-bank-account.md) | `PUT /supplierbankaccount` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Create VAT Code](actions/create-vat-code.md) | `PUT /vatcode` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Invoice Account Coding Queue](actions/delete-invoice-account-coding-queue.md) | `DELETE /invoiceaccountcodingqueue/:invoiceaccountcodingqueueid` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Invoice Diary](actions/delete-invoice-diary.md) | `DELETE /invoice/diary/:invoiceDiaryId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Invoice Diary Attachment](actions/delete-invoice-diary-attachment.md) | `DELETE /invoice/diary/attachment/:invoiceDiaryId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Invoice Queue Record](actions/delete-invoice-queue-record.md) | `DELETE /invoicequeue/:invoiceQueueId/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Locked Row](actions/delete-locked-row.md) | `DELETE /lockedRow/:RowId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Delete Locked Rows](actions/delete-locked-rows.md) | `DELETE /lockedRow` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Download Payment Image](actions/download-payment-image.md) | `GET /payment/images/download` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Generate InvoiceDiaryAttachmentsSasToken](actions/generate-invoice-diary-attachments-sas-token.md) | `GET /InvoiceDiaryAttachmentsSasToken` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Generate InvoiceImageFilePathSasToken](actions/generate-invoice-image-file-path-sas-token.md) | `GET /InvoiceImagesFilePathSasToken` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Generate InvoiceImagesSasToken](actions/generate-invoice-images-sas-token.md) | `GET /InvoiceImagesSasToken` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Generate InvoiceQueueImagesSasToken](actions/generate-invoice-queue-images-sas-token.md) | `GET /InvoiceQueueImagesSasToken` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Invoice Account Coding History](actions/get-invoice-account-coding-history.md) | `GET /invoice/:invoiceId/invoiceAccountCodingLog/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Invoice Account Coding Queue](actions/get-invoice-account-coding-queue.md) | `GET /invoicequeue/:invoiceQueueId/invoiceAccountCodingQueue/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Invoice Details](actions/get-invoice-details.md) | `GET /invoice/detail` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Invoice Log Table Metadata](actions/get-invoice-log-table-metadata.md) | `GET /invoicequeue/metadata/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Invoice Queue](actions/get-invoice-queue.md) | `GET /invoicequeue/:invoiceQueueId/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get Language](actions/get-language.md) | `GET /language/:LanguageID` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Get User Preferences](actions/get-user-preferences.md) | `GET /preferences` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Inquire Invoice For Role](actions/inquire-invoice-for-role.md) | `POST /invoice/inquire/:invoiceId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Accounts By Role](actions/list-accounts-by-role.md) | `GET /account/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Allocation Types For Role](actions/list-allocation-types-for-role.md) | `GET /allocationType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Asset Types For Role](actions/list-asset-types-for-role.md) | `GET /assettype/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Assets By Role](actions/list-assets-by-role.md) | `GET /asset/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Companies By Role](actions/list-companies-by-role.md) | `GET /company/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Currencies](actions/list-currencies.md) | `GET /currency` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Flow Proposal For Role](actions/list-flow-proposal-for-role.md) | `GET /invoice/FlowProposal/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Group Types](actions/list-group-types.md) | `GET /groupType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Account Coding Posts](actions/list-invoice-account-coding-posts.md) | `GET /invoice/accountcoding` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Account Coding Posts Batch](actions/list-invoice-account-coding-posts-batch.md) | `POST /invoice/accountcoding` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Account Coding Queue](actions/list-invoice-account-coding-queue.md) | `GET /invoiceaccountcodingqueue/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Diary Posts](actions/list-invoice-diary-posts.md) | `GET /invoice/diary` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Diary Posts By Invoice](actions/list-invoice-diary-posts-by-invoice.md) | `GET /invoice/:invoiceId/diary` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Flow Posts](actions/list-invoice-flow-posts.md) | `GET /invoice/flow` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Purchase Orders](actions/list-invoice-purchase-orders.md) | `POST /invoicepurchaseorder/ListInvoicePurchaseOrder` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoice Queue](actions/list-invoice-queue.md) | `GET /invoicequeue/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Languages](actions/list-languages.md) | `GET /language` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Licences](actions/list-licences.md) | `GET /licence` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Locked Rows](actions/list-locked-rows.md) | `GET /lockedRow` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Object Relation](actions/list-object-relation.md) | `GET /objectRelation` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Object Relation Setting](actions/list-object-relation-setting.md) | `GET /objectRelationSetting` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Object Types](actions/list-object-types.md) | `GET /objectType` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Objects For Role](actions/list-objects-for-role.md) | `GET /object/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Approvals](actions/list-payment-approvals.md) | `GET /payment/approval` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Audit Logs](actions/list-payment-audit-logs.md) | `GET /payment/audit` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | `GET /payment/configuration/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Images](actions/list-payment-images.md) | `GET /payment/images` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Permissions](actions/list-payment-permissions.md) | `GET /payment/permission` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Schedules](actions/list-payment-schedules.md) | `GET /payment/schedule` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Statuses](actions/list-payment-statuses.md) | `GET /payment/status` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Supplier Statuses](actions/list-payment-supplier-statuses.md) | `GET /payment/supplier/status` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Suppliers](actions/list-payment-suppliers.md) | `GET /payment/supplier` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Tenant Company Configurations](actions/list-payment-tenant-company-configurations.md) | `GET /payment/configuration/tenant/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Tenant Configurations](actions/list-payment-tenant-configurations.md) | `GET /payment/configuration/tenant` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payment Tenant Provider Configurations](actions/list-payment-tenant-provider-configurations.md) | `GET /payment/configuration/tenant/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Payments](actions/list-payments.md) | `GET /payment` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Pending Supplier Payments](actions/list-pending-supplier-payments.md) | `GET /payment/supplier/payments/pending` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Periods For Role](actions/list-periods-for-role.md) | `GET /period/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Purchase Order Deliveries For Import In Queue](actions/list-purchase-order-deliveries-for-import-in-queue.md) | `POST /purchaseorderdeliveryqueue/ListPurchaseOrderDeliveryForImportInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Purchase Order Deliveries In Snapshot Queue](actions/list-purchase-order-deliveries-in-snapshot-queue.md) | `POST /purchaseorderdeliveryqueue/ListPurchaseOrderDeliveryInSnapshotQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Purchase Orders For Export In Queue](actions/list-purchase-orders-for-export-in-queue.md) | `POST /purchaseorderqueue/ListPurchaseOrderForExportInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Purchase Orders For Import In Queue](actions/list-purchase-orders-for-import-in-queue.md) | `POST /purchaseorderqueue/ListPurchaseOrderForImportInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Purchase Orders In Snapshot Queue](actions/list-purchase-orders-in-snapshot-queue.md) | `POST /purchaseorderqueue/ListPurchaseOrderInSnapshotQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Role Operation Permissions](actions/list-role-operation-permissions.md) | `GET /role/operationpermissiongroup` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Roles](actions/list-roles.md) | `GET /role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List Suppliers For Role](actions/list-suppliers-for-role.md) | `GET /supplier/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [List VAT Codes For Role](actions/list-vat-codes-for-role.md) | `GET /vatcode/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Match Invoice Queue Records](actions/match-invoice-queue-records.md) | `POST /invoicequeue/match` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Place Purchase Order Deliveries In Snapshot Queue](actions/place-purchase-order-deliveries-in-snapshot-queue.md) | `PUT /purchaseorderdeliveryqueue/PlacePurchaseOrderDeliveriesInSnapshotQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Place Purchase Orders In Snapshot Queue](actions/place-purchase-orders-in-snapshot-queue.md) | `PUT /purchaseorderqueue/PlacePurchaseOrderInSnapshotQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Account In Queue](actions/process-account-in-queue.md) | `PUT /account/ProcessAccountInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Asset In Queue](actions/process-asset-in-queue.md) | `PUT /asset/ProcessAssetInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Asset Type In Queue](actions/process-asset-type-in-queue.md) | `PUT /assettype/ProcessAssetTypeInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Code Relation In Queue](actions/process-code-relation-in-queue.md) | `PUT /coderelation/ProcessCodeRelationInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Commodity In Queue](actions/process-commodity-in-queue.md) | `PUT /commodity/ProcessCommodityInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Company In Queue](actions/process-company-in-queue.md) | `PUT /company/ProcessCompanyInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Currency In Queue](actions/process-currency-in-queue.md) | `PUT /currency/ProcessCurrencyInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Holiday In Queue](actions/process-holiday-in-queue.md) | `PUT /holiday/ProcessHolidayInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Object In Queue](actions/process-object-in-queue.md) | `PUT /object/ProcessObjectInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Object Type In Queue](actions/process-object-type-in-queue.md) | `PUT /objecttype/ProcessObjectTypeInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Payments](actions/process-payments.md) | `POST /payment/process` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Period Queue Records](actions/process-period-queue-records.md) | `PUT /period/ProcessPeriodInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Supplier Bank Account In Queue](actions/process-supplier-bank-account-in-queue.md) | `PUT /supplierbankaccount/ProcessSupplierBankAccountInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process Supplier Queue Records](actions/process-supplier-queue-records.md) | `PUT /supplier/ProcessSupplierInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Process VAT Code In Queue](actions/process-vat-code-in-queue.md) | `PUT /vatcode/ProcessVatCodeInQueue` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Reject Invoice For Role](actions/reject-invoice-for-role.md) | `POST /invoice/reject/:invoiceId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Resend Payments](actions/resend-payments.md) | `POST /payment/process/resend` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Save A New Diary Attachment Image](actions/save-a-new-diary-attachment-image.md) | `POST /InvoiceDiaryAttachments` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Search For Expenditures](actions/search-for-expenditures.md) | `GET /budget/search/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | `GET /payment/supplier/typeahead` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Transfer Invoice Queue Records](actions/transfer-invoice-queue-records.md) | `POST /invoicequeue/transfer` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Unknown Invoice For Role](actions/unknown-invoice-for-role.md) | `POST /invoice/unknown/:invoiceId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Invoice Account Coding Queue](actions/update-invoice-account-coding-queue.md) | `PUT /invoiceaccountcodingqueue/:invoiceaccountcodingqueueid` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Invoice Details](actions/update-invoice-details.md) | `POST /invoice/detail` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Invoice Diary Post](actions/update-invoice-diary-post.md) | `PUT /invoice/:invoiceId/diary/:diaryId` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Invoice Queue Transfer Flag](actions/update-invoice-queue-transfer-flag.md) | `POST /invoicequeue/updatetransferflag/transfer/:transfer/role/:role` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Payment Supplier](actions/update-payment-supplier.md) | `PUT /payment/supplier` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
| [Update Payment Suppliers](actions/update-payment-suppliers.md) | `PUT /payment/suppliers` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html) |
