# <img src="https://images.mindcloud.co/apps/icons/images-2_1783094673766.png" alt="Rillion Prime logo" width="28" height="28"> Rillion Prime: Universal API

Rillion Prime through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rillionPrime/latest
- **Actions:** 140
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rillion.com/
- **Vendor API docs:** https://rillion-prime-integration.readme.io/docs/using-the-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Roles](actions/list-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (140)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate InvoiceImageFilePathSasToken](actions/generate-invoice-image-file-path-sas-token.md) | GET |  |
| [Generate InvoiceImagesSasToken](actions/generate-invoice-images-sas-token.md) | GET |  |
| [Generate InvoiceQueueImagesSasToken](actions/generate-invoice-queue-images-sas-token.md) | GET |  |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [List Accounts By Role](actions/list-accounts-by-role.md) | GET |  |
| [Process Account In Queue](actions/process-account-in-queue.md) | PUT |  |

### Accounting Periods

| Action | Method | Description |
| --- | --- | --- |
| [Create Period Queue Record](actions/create-period-queue-record.md) | POST |  |
| [List Periods For Role](actions/list-periods-for-role.md) | GET |  |
| [Process Period Queue Records](actions/process-period-queue-records.md) | PUT |  |

### Allocation Type

| Action | Method | Description |
| --- | --- | --- |
| [List Allocation Types For Role](actions/list-allocation-types-for-role.md) | GET |  |

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Approval](actions/create-payment-approval.md) | POST |  |
| [List Payment Approvals](actions/list-payment-approvals.md) | GET |  |

### Asset Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset Type](actions/create-asset-type.md) | POST |  |
| [List Asset Types For Role](actions/list-asset-types-for-role.md) | GET |  |
| [Process Asset Type In Queue](actions/process-asset-type-in-queue.md) | PUT |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST |  |
| [List Assets By Role](actions/list-assets-by-role.md) | GET |  |
| [Process Asset In Queue](actions/process-asset-in-queue.md) | PUT |  |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Copy Invoice Diary Attachments](actions/copy-invoice-diary-attachments.md) | POST |  |
| [Delete Invoice Diary Attachment](actions/delete-invoice-diary-attachment.md) | DELETE |  |
| [Generate InvoiceDiaryAttachmentsSasToken](actions/generate-invoice-diary-attachments-sas-token.md) | GET |  |
| [Save A New Diary Attachment Image](actions/save-a-new-diary-attachment-image.md) | POST |  |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Audit Logs](actions/list-payment-audit-logs.md) | GET |  |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier Bank Account](actions/create-supplier-bank-account.md) | POST |  |
| [Process Supplier Bank Account In Queue](actions/process-supplier-bank-account-in-queue.md) | PUT |  |

### Code Relation

| Action | Method | Description |
| --- | --- | --- |
| [Create Code Relation](actions/create-code-relation.md) | POST |  |
| [Process Code Relation In Queue](actions/process-code-relation-in-queue.md) | PUT |  |

### Commodity

| Action | Method | Description |
| --- | --- | --- |
| [Create Commodity](actions/create-commodity.md) | POST |  |
| [Process Commodity In Queue](actions/process-commodity-in-queue.md) | PUT |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [List Companies By Role](actions/list-companies-by-role.md) | GET |  |
| [Process Company In Queue](actions/process-company-in-queue.md) | PUT |  |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Create Currency](actions/create-currency.md) | POST |  |
| [List Currencies](actions/list-currencies.md) | GET |  |
| [Process Currency In Queue](actions/process-currency-in-queue.md) | PUT |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Search For Expenditures](actions/search-for-expenditures.md) | GET |  |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Export Job](actions/create-payment-export-job.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Payment Image](actions/download-payment-image.md) | GET |  |
| [List Payment Images](actions/list-payment-images.md) | GET |  |

### Group Type

| Action | Method | Description |
| --- | --- | --- |
| [List Group Types](actions/list-group-types.md) | GET |  |

### Holiday

| Action | Method | Description |
| --- | --- | --- |
| [Create Holiday](actions/create-holiday.md) | POST |  |
| [Process Holiday In Queue](actions/process-holiday-in-queue.md) | PUT |  |

### Invoice Account Coding Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Account Coding History](actions/get-invoice-account-coding-history.md) | GET |  |
| [List Invoice Account Coding Posts](actions/list-invoice-account-coding-posts.md) | GET |  |
| [List Invoice Account Coding Posts Batch](actions/list-invoice-account-coding-posts-batch.md) | PUT |  |

### Invoice Diary Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice Diary Post](actions/create-invoice-diary-post.md) | POST |  |
| [Create Invoice Diary Post By Invoice](actions/create-invoice-diary-post-by-invoice.md) | POST |  |
| [List Invoice Diary Posts](actions/list-invoice-diary-posts.md) | GET |  |
| [List Invoice Diary Posts By Invoice](actions/list-invoice-diary-posts-by-invoice.md) | GET |  |
| [Update Invoice Diary Post](actions/update-invoice-diary-post.md) | PUT |  |

### Invoice Flow Post

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Flow Posts](actions/list-invoice-flow-posts.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Approve Invoice For Role](actions/approve-invoice-for-role.md) | PUT |  |
| [Approve Invoices For Roles](actions/approve-invoices-for-roles.md) | PUT |  |
| [Auto Match Invoices](actions/auto-match-invoices.md) | PUT |  |
| [Calculate Vat Account Coding For Invoice](actions/calculate-vat-account-coding-for-invoice.md) | PUT |  |
| [Cancel Invoice For Role](actions/cancel-invoice-for-role.md) | PUT |  |
| [Change Invoice Payment Dates By Company Supplier And Invoice Number](actions/change-invoice-payment-dates-by-company-supplier-and-invoice-number.md) | PUT |  |
| [Change Invoice Payment Dates By Series And Number](actions/change-invoice-payment-dates-by-series-and-number.md) | PUT |  |
| [Delete Invoice Diary](actions/delete-invoice-diary.md) | DELETE |  |
| [Get Invoice Details](actions/get-invoice-details.md) | GET |  |
| [Inquire Invoice For Role](actions/inquire-invoice-for-role.md) | PUT |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Reject Invoice For Role](actions/reject-invoice-for-role.md) | PUT |  |
| [Unknown Invoice For Role](actions/unknown-invoice-for-role.md) | PUT |  |
| [Update Invoice Details](actions/update-invoice-details.md) | PUT |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get Language](actions/get-language.md) | GET |  |
| [List Languages](actions/list-languages.md) | GET |  |

### Licence

| Action | Method | Description |
| --- | --- | --- |
| [Create Licences](actions/create-licences.md) | POST |  |
| [List Licences](actions/list-licences.md) | GET |  |

### Locked Row

| Action | Method | Description |
| --- | --- | --- |
| [Create Locked Rows](actions/create-locked-rows.md) | POST |  |
| [Delete Locked Row](actions/delete-locked-row.md) | DELETE |  |
| [Delete Locked Rows](actions/delete-locked-rows.md) | DELETE |  |
| [List Locked Rows](actions/list-locked-rows.md) | GET |  |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [Create Object](actions/create-object.md) | POST |  |
| [List Objects For Role](actions/list-objects-for-role.md) | GET |  |
| [Process Object In Queue](actions/process-object-in-queue.md) | PUT |  |

### Object Relation

| Action | Method | Description |
| --- | --- | --- |
| [List Object Relation](actions/list-object-relation.md) | GET |  |

### Object Relation Setting

| Action | Method | Description |
| --- | --- | --- |
| [List Object Relation Setting](actions/list-object-relation-setting.md) | GET |  |

### Object Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Object Type](actions/create-object-type.md) | POST |  |
| [List Object Types](actions/list-object-types.md) | GET |  |
| [Process Object Type In Queue](actions/process-object-type-in-queue.md) | PUT |  |

### Payment Configuration Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Configuration Company](actions/create-payment-configuration-company.md) | POST |  |

### Payment Configuration Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | GET |  |

### Payment Creation Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Creation Trigger](actions/create-payment-creation-trigger.md) | POST |  |

### Payment Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Supplier Grouping](actions/create-payment-supplier-grouping.md) | POST |  |
| [List Payment Suppliers](actions/list-payment-suppliers.md) | GET |  |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | GET |  |
| [Update Payment Supplier](actions/update-payment-supplier.md) | PUT |  |
| [Update Payment Suppliers](actions/update-payment-suppliers.md) | PUT |  |

### Payment Tenant Company Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Tenant Company Configuration](actions/create-payment-tenant-company-configuration.md) | POST |  |
| [List Payment Tenant Company Configurations](actions/list-payment-tenant-company-configurations.md) | GET |  |

### Payment Tenant Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Tenant Configuration](actions/create-payment-tenant-configuration.md) | POST |  |
| [List Payment Tenant Configurations](actions/list-payment-tenant-configurations.md) | GET |  |

### Payment Tenant Provider Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Tenant Provider Configuration](actions/create-payment-tenant-provider-configuration.md) | POST |  |
| [List Payment Tenant Provider Configurations](actions/list-payment-tenant-provider-configurations.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Approve Payments](actions/approve-payments.md) | PUT |  |
| [Cancel Payments](actions/cancel-payments.md) | PUT |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [List Pending Supplier Payments](actions/list-pending-supplier-payments.md) | GET |  |
| [Process Payments](actions/process-payments.md) | PUT |  |
| [Resend Payments](actions/resend-payments.md) | PUT |  |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Permissions](actions/list-payment-permissions.md) | GET |  |
| [List Role Operation Permissions](actions/list-role-operation-permissions.md) | GET |  |

### Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get User Preferences](actions/get-user-preferences.md) | GET |  |

### Proposals

| Action | Method | Description |
| --- | --- | --- |
| [List Flow Proposal For Role](actions/list-flow-proposal-for-role.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Purchase Orders](actions/list-invoice-purchase-orders.md) | POST |  |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [Add Invoice Receipt To Invoice Queue](actions/add-invoice-receipt-to-invoice-queue.md) | POST |  |
| [Change Invoice Queue Account Coding Date](actions/change-invoice-queue-account-coding-date.md) | PUT |  |
| [Create Invoice Queue](actions/create-invoice-queue.md) | PUT |  |
| [Create Purchase Order Delivery Queue Records](actions/create-purchase-order-delivery-queue-records.md) | POST |  |
| [Create Purchase Order Queue Records](actions/create-purchase-order-queue-records.md) | POST |  |
| [Delete Invoice Account Coding Queue](actions/delete-invoice-account-coding-queue.md) | DELETE |  |
| [Delete Invoice Queue Record](actions/delete-invoice-queue-record.md) | DELETE |  |
| [Get Invoice Account Coding Queue](actions/get-invoice-account-coding-queue.md) | GET |  |
| [Get Invoice Log Table Metadata](actions/get-invoice-log-table-metadata.md) | GET |  |
| [Get Invoice Queue](actions/get-invoice-queue.md) | GET |  |
| [List Invoice Account Coding Queue](actions/list-invoice-account-coding-queue.md) | GET |  |
| [List Invoice Queue](actions/list-invoice-queue.md) | GET |  |
| [List Purchase Order Deliveries For Import In Queue](actions/list-purchase-order-deliveries-for-import-in-queue.md) | GET |  |
| [List Purchase Order Deliveries In Snapshot Queue](actions/list-purchase-order-deliveries-in-snapshot-queue.md) | GET |  |
| [List Purchase Orders For Export In Queue](actions/list-purchase-orders-for-export-in-queue.md) | GET |  |
| [List Purchase Orders For Import In Queue](actions/list-purchase-orders-for-import-in-queue.md) | GET |  |
| [List Purchase Orders In Snapshot Queue](actions/list-purchase-orders-in-snapshot-queue.md) | GET |  |
| [Match Invoice Queue Records](actions/match-invoice-queue-records.md) | PUT |  |
| [Place Purchase Order Deliveries In Snapshot Queue](actions/place-purchase-order-deliveries-in-snapshot-queue.md) | PUT |  |
| [Place Purchase Orders In Snapshot Queue](actions/place-purchase-orders-in-snapshot-queue.md) | PUT |  |
| [Transfer Invoice Queue Records](actions/transfer-invoice-queue-records.md) | PUT |  |
| [Update Invoice Account Coding Queue](actions/update-invoice-account-coding-queue.md) | PUT |  |
| [Update Invoice Queue Transfer Flag](actions/update-invoice-queue-transfer-flag.md) | PUT |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Schedule](actions/create-payment-schedule.md) | POST |  |
| [List Payment Schedules](actions/list-payment-schedules.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET |  |
| [List Payment Supplier Statuses](actions/list-payment-supplier-statuses.md) | GET |  |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST |  |
| [List Suppliers For Role](actions/list-suppliers-for-role.md) | GET |  |
| [Process Supplier Queue Records](actions/process-supplier-queue-records.md) | PUT |  |

### Vat Code

| Action | Method | Description |
| --- | --- | --- |
| [Create VAT Code](actions/create-vat-code.md) | POST |  |
| [List VAT Codes For Role](actions/list-vat-codes-for-role.md) | GET |  |
| [Process VAT Code In Queue](actions/process-vat-code-in-queue.md) | PUT |  |

