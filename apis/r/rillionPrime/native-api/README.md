# Rillion Prime Pay: Native API Reference

A consolidated summary of Rillion Prime Pay's API configuration and 30 documented operations, with links to official documentation.

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

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Payments](actions/approve-payments.md) | `POST /payment/process/approve` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Cancel Payments](actions/cancel-payments.md) | `POST /payment/process/cancel` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Approval](actions/create-payment-approval.md) | `POST /payment/approval` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Configuration Company](actions/create-payment-configuration-company.md) | `POST /payment/configuration/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Export Job](actions/create-payment-export-job.md) | `POST /payment/export` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Schedule](actions/create-payment-schedule.md) | `POST /payment/schedule` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Supplier Grouping](actions/create-payment-supplier-grouping.md) | `POST /payment/suppliers/grouping` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Tenant Company Configuration](actions/create-payment-tenant-company-configuration.md) | `POST /payment/configuration/tenant/company` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Tenant Configuration](actions/create-payment-tenant-configuration.md) | `POST /payment/configuration/tenant` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Create Payment Tenant Provider Configuration](actions/create-payment-tenant-provider-configuration.md) | `POST /payment/configuration/tenant/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Download Payment Image](actions/download-payment-image.md) | `GET /payment/images/download` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Approvals](actions/list-payment-approvals.md) | `GET /payment/approval` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Audit Logs](actions/list-payment-audit-logs.md) | `GET /payment/audit` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Configuration Providers](actions/list-payment-configuration-providers.md) | `GET /payment/configuration/provider` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [List Payment Images](actions/list-payment-images.md) | `GET /payment/images` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
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
| [Process Payments](actions/process-payments.md) | `POST /payment/process` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Resend Payments](actions/resend-payments.md) | `POST /payment/process/resend` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Search Payment Suppliers](actions/search-payment-suppliers.md) | `GET /payment/supplier/typeahead` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Update Payment Supplier](actions/update-payment-supplier.md) | `PUT /payment/supplier` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
| [Update Payment Suppliers](actions/update-payment-suppliers.md) | `PUT /payment/suppliers` | [docs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0) |
