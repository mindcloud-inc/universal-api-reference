# <img src="https://images.mindcloud.co/apps/icons/images-2_1783094673766.png" alt="Rillion Prime Pay logo" width="28" height="28"> Rillion Prime Pay: Universal API

Connect to the Rillion Prime Pay API to manage payment approvals, schedules, suppliers, statuses, exports, and related payment operations from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rillionPrime/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rillion.com/
- **Vendor API docs:** https://rillion-prime-integration.readme.io/docs/using-the-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payments](actions/list-payments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Audit

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Audit Logs](actions/list-payment-audit-logs.md) | GET |  |

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | GET |  |
| [List Payment Tenant Company Configurations](actions/list-payment-tenant-company-configurations.md) | GET |  |
| [List Payment Tenant Configurations](actions/list-payment-tenant-configurations.md) | GET |  |
| [List Payment Tenant Provider Configurations](actions/list-payment-tenant-provider-configurations.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Approve Payments](actions/approve-payments.md) | PUT |  |
| [Cancel Payments](actions/cancel-payments.md) | PUT |  |
| [Create Payment Approval](actions/create-payment-approval.md) | POST |  |
| [Create Payment Export Job](actions/create-payment-export-job.md) | POST |  |
| [Create Payment Schedule](actions/create-payment-schedule.md) | POST |  |
| [Download Payment Image](actions/download-payment-image.md) | GET |  |
| [List Payment Approvals](actions/list-payment-approvals.md) | GET |  |
| [List Payment Images](actions/list-payment-images.md) | GET |  |
| [List Payment Permissions](actions/list-payment-permissions.md) | GET |  |
| [List Payment Schedules](actions/list-payment-schedules.md) | GET |  |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [Process Payments](actions/process-payments.md) | PUT |  |
| [Resend Payments](actions/resend-payments.md) | PUT |  |

### Suppliers

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Supplier Statuses](actions/list-payment-supplier-statuses.md) | GET |  |
| [List Payment Suppliers](actions/list-payment-suppliers.md) | GET |  |
| [List Pending Supplier Payments](actions/list-pending-supplier-payments.md) | GET |  |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | GET |  |
| [Update Payment Supplier](actions/update-payment-supplier.md) | PUT |  |
| [Update Payment Suppliers](actions/update-payment-suppliers.md) | PUT |  |

