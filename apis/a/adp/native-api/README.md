# ADP: Native API Reference

A consolidated summary of ADP's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developers.adp.com/build/api-explorer
- **API base URL:** `https://api.adp.com/`

## Authentication

### OAuth 2.0

For the private key, copy the text between "-----BEGIN PRIVATE KEY-----" and "-----END PRIVATE KEY-----".
For the certificate, copy the text between "-----BEGIN CERTIFICATE-----" and "-----END CERTIFICATE-----"

### Credentials

- **Client Private Key:** `key` · required · The private key file used for mutual TLS client authentication. This is your client's private key that proves your identity to the OAuth2 server. Must be in PEM format.
- **Client Certificate:** `cert` · required · The client certificate file used for mutual TLS authentication. This is your client's public certificate that contains your identity information, signed by a trusted CA. Must be in PEM format and registered with the OAuth2 server.
- **Certificate Authority (CA):** `ca` · optional · The Certificate Authority (CA) certificate used in mutual TLS to verify the OAuth2 server's identity. This helps prevent man-in-the-middle attacks by ensuring you're connecting to the legitimate authorization server. Must be in PEM format.
- **Reject Unauthorized:** `rejectUnauthorized` · optional · Controls certificate validation in mutual TLS. When true (recommended for production), the OAuth2 server's certificate must be valid and trusted. When false, invalid or self-signed certificates are accepted, which should only be used in development/testing.
- **Client Id:** `clientId` · required
- **Client Secret:** `clientSecret` · required

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://accounts.adp.com/auth/oauth/v2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured. The token flow requires mutual TLS.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–50). Use `$skip` in the query string as the record offset.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Payroll Batch](actions/create-payroll-batch.md) | `POST events/payroll/v1/pay-data-input.modify` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-data-input-v1-pay-data-input?operation=POST%2Fevents%2Fpayroll%2Fv1%2Fpay-data-input.modify#swagger) |
| [Create Time Card](actions/create-time-card.md) | `POST events/time/v2/time-entries.modify` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-time-time-cards-v2-time-cards?operation=POST%2Fevents%2Ftime%2Fv2%2Ftime-entries.modify#swagger) |
| [Get Payroll Earning Allocations](actions/get-payroll-earning-allocations.md) | `GET payroll/v2/payroll-output/:outputId/associate-payment-allocations/earnings` | [docs](https://marketplace-cdn.adp.com/dev-portal/pdf/protected/Payroll_Output_API_Guide_for_RUN_Powered_by_ADP) |
| [Get Payroll Metadata](actions/get-payroll-meta-data.md) | `GET events/payroll/v1/pay-data-input.modify/meta` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-data-input-v1-pay-data-input?operation=GET%2Fevents%2Fpayroll%2Fv1%2Fpay-data-input.modify%2Fmeta#swagger) |
| [Get Worker](actions/get-worker.md) | `GET hr/v2/workers/:aOid` | [docs](https://api-central.adp.com/projects/735093bcc595cb7d5328f9fb6494a4bec696ce0fb6a0f33f) |
| [List Workers](actions/get-workers.md) | `GET hr/v2/workers` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-hr-workers-v2-workers?operation=GET%2Fhr%2Fv2%2Fworkers#swagger) |
| [List Associate Work Locations](actions/list-associate-work-locations.md) | `GET /hcm/v1/validation-tables/associate-work-locations` | [docs](https://api-central.adp.com/projects/735093bcc595cb7d5328f9fb6494a4bec696ce0fb6a0f33f) |
| [List Business Units](actions/list-business-units.md) | `GET hcm/v1/validation-tables/business-units` | [docs](https://api-central.adp.com/projects/735093bcc595cb7d5328f9fb6494a4bec696ce0fb6a0f33f) |
| [List Pay Data Input](actions/list-pay-data-input.md) | `GET events/payroll/v1/pay-data-input.modify/meta` |  |
| [List Payroll Groups](actions/list-payroll-groups.md) | `GET payroll/v1/pay-schedule/payroll-groups` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-payroll-group-pay-periods-v1-payroll-group-pay-periods?operation=GET%2Fpayroll%2Fv1%2Fpay-schedule%2Fpayroll-groups#swagger) |
| [List Payroll Outputs](actions/list-payroll-outputs.md) | `GET payroll/v2/payroll-output` | [docs](https://marketplace-cdn.adp.com/dev-portal/pdf/protected/Payroll_Output_API_Guide_for_RUN_Powered_by_ADP) |
| [List Time Cards by Associate ID](actions/list-time-cards-by-associate-id.md) | `GET time/v2/workers/:employeeAOID/time-cards` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn.next.gen/hcm-offrg-wfn.next.gen-time-time-cards-v2-time-cards?operation=GET%2Fevents%2Ftime%2Fv2%2Ftime-entries.modify%2F%7Bevent-id%7D#swagger) |
| [List Worker Leaves](actions/list-worker-leaves.md) | `GET hr/v2/workers/:aoid/leaves` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-hr-worker-leaves-v2-worker-leaves?operation=GET%2Fhr%2Fv2%2Fworkers%2F%7Baoid%7D%2Fleaves#swagger) |
| [Get Worker Pay Statement](actions/list-worker-pay-statement-by-uri.md) | `GET payroll/v1/workers/:aoid/organizational-pay-statements/:payStatementId` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-statements-v1-pay-statements?operation=GET%2Fpayroll%2Fv1%2Fworkers%2F%7Baoid%7D%2Forganizational-pay-statements%2F%7Bpay-statement-id%7D#swagger) |
| [List Worker Pay Statements](actions/list-worker-pay-statements.md) | `GET payroll/v1/workers/:aoid/organizational-pay-statements` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-statements-v1-pay-statements?operation=GET%2Fpayroll%2Fv1%2Fworkers%2F%7Baoid%7D%2Forganizational-pay-statements#swagger) |
| [List Worker Time Off Balances](actions/list-worker-time-off-balances.md) | `GET time/v2/workers/:aoid/time-off-details/time-off-balances` | [docs](https://marketplace-cdn.adp.com/dev-portal/pdf/protected/Time_Off_Balances_API_Guide_for_ADP_Workforce_Now) |
| [List Worker Time Off Requests](actions/list-worker-time-off-requests.md) | `GET time/v2/workers/:aoid/time-off-details/time-off-requests` | [docs](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-time-time-off-requests-v2-time-off-requests?operation=GET%2Ftime%2Fv2%2Fworkers%2F%7Baoid%7D%2Ftime-off-details%2Ftime-off-requests#swagger) |
