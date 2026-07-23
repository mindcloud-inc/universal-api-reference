# <img src="https://images.mindcloud.co/apps/icons/images-2_1783094673766.png" alt="Rillion Prime logo" width="28" height="28"> Rillion Prime: Universal API

Rillion Prime through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rillionPrime/latest
- **Actions:** 40
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

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts By Role](actions/list-accounts-by-role.md) | GET |  |

### Allocation Type

| Action | Method | Description |
| --- | --- | --- |
| [List Allocation Types For Role](actions/list-allocation-types-for-role.md) | GET |  |

### Asset Type

| Action | Method | Description |
| --- | --- | --- |
| [List Asset Types For Role](actions/list-asset-types-for-role.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies By Role](actions/list-companies-by-role.md) | GET |  |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Search For Expenditures](actions/search-for-expenditures.md) | GET |  |

### Group Type

| Action | Method | Description |
| --- | --- | --- |
| [List Group Types](actions/list-group-types.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Details](actions/get-invoice-details.md) | GET |  |
| [Get Invoice Log Table Metadata](actions/get-invoice-log-table-metadata.md) | GET |  |
| [Get Invoice Queue](actions/get-invoice-queue.md) | GET |  |
| [List Invoice Queue](actions/list-invoice-queue.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Get Language](actions/get-language.md) | GET |  |
| [List Languages](actions/list-languages.md) | GET |  |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [List Object Relation](actions/list-object-relation.md) | GET |  |
| [List Object Relation Setting](actions/list-object-relation-setting.md) | GET |  |
| [List Object Types](actions/list-object-types.md) | GET |  |
| [List Objects For Role](actions/list-objects-for-role.md) | GET |  |

### Payment Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Suppliers](actions/list-payment-suppliers.md) | GET |  |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | GET |  |

### Payment Tenant Company Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Tenant Company Configurations](actions/list-payment-tenant-company-configurations.md) | GET |  |

### Payment Tenant Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Tenant Configurations](actions/list-payment-tenant-configurations.md) | GET |  |

### Payment Tenant Provider Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Tenant Provider Configurations](actions/list-payment-tenant-provider-configurations.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Approvals](actions/list-payment-approvals.md) | GET |  |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | GET |  |
| [List Payment Permissions](actions/list-payment-permissions.md) | GET |  |
| [List Payment Schedules](actions/list-payment-schedules.md) | GET |  |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET |  |
| [List Payment Supplier Statuses](actions/list-payment-supplier-statuses.md) | GET |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [List Pending Supplier Payments](actions/list-pending-supplier-payments.md) | GET |  |

### Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get User Preferences](actions/get-user-preferences.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order Delivery Queue Records](actions/create-purchase-order-delivery-queue-records.md) | POST |  |
| [List Purchase Order Deliveries For Import In Queue](actions/list-purchase-order-deliveries-for-import-in-queue.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Flow Proposal For Role](actions/list-flow-proposal-for-role.md) | GET |  |
| [List Periods For Role](actions/list-periods-for-role.md) | GET |  |
| [List Role Operation Permissions](actions/list-role-operation-permissions.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers For Role](actions/list-suppliers-for-role.md) | GET |  |

### Vat Code

| Action | Method | Description |
| --- | --- | --- |
| [List VAT Codes For Role](actions/list-vat-codes-for-role.md) | GET |  |

