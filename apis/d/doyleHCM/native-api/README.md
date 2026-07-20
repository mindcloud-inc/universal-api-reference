# Doyle HCM: Native API Reference

A consolidated summary of Doyle HCM's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.worklio.com/docs/how-to-get-api-access
- **API base URL:** `https://api.worklio.com`

## Authentication

### OAuth 2.0

Doyle HCM uses Worklio direct-mode OAuth 2.0 Resource Owner flow for server-to-server API access.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.worklio.com/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.worklio.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `api`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://apidocs.worklio.com/docs/how-to-get-api-access)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `api-version` | `1.0` |
| `x-api-version` | `1.0` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create company department](actions/create-company-department.md) | `POST /wep/companies/:companyId/departments` | [docs](https://apidocs.worklio.com/reference/post_wep-companies-companyid-departments) |
| [Create company position](actions/create-company-position.md) | `POST /wep/companies/:companyId/positions` | [docs](https://apidocs.worklio.com/reference/post_wep-companies-companyid-positions) |
| [Get company](actions/get-company.md) | `GET /wep/companies/:companyId` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid.md) |
| [Get company access policy](actions/get-company-access-policy.md) | `GET /wep/companies/:companyId/access-policy` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-access-policy) |
| [Get company dashboard](actions/get-company-dashboard.md) | `GET /wep/companies/:companyId/dashboard` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-dashboard-1) |
| [Get company department](actions/get-company-department.md) | `GET /wep/companies/:companyId/departments/:departmentId` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-departments-departmentid) |
| [Get company KYC document type](actions/get-company-kyc-document-type.md) | `GET /wep/companies/:companyId/kyc/documenttypes/:key` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-kyc-documenttypes-key) |
| [Get company KYC status](actions/get-company-kyc-status.md) | `GET /wep/companies/:companyId/kyc` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-kyc) |
| [Get company work location](actions/get-company-work-location.md) | `GET /wep/companies/:companyId/worklocations/:wlocationId` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-worklocations-wlocationid-1) |
| [Get current user](actions/get-current-user.md) | `GET /wep/me` | [docs](https://apidocs.worklio.com/reference/get_wep-me) |
| [Get dashboard](actions/get-dashboard.md) | `GET /wep/dashboard` | [docs](https://apidocs.worklio.com/reference/get_wep-dashboard-1) |
| [List companies](actions/list-companies.md) | `GET /wep/companies` | [docs](https://apidocs.worklio.com/reference/get_wep-companies) |
| [List company departments](actions/list-company-departments.md) | `GET /wep/companies/:companyId/departments` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-departments) |
| [List company KYC document types](actions/list-company-kyc-document-types.md) | `GET /wep/companies/:companyId/kyc/documenttypes` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-kyc-documenttypes) |
| [List company positions](actions/list-company-positions.md) | `GET /wep/companies/:companyId/positions` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-positions) |
| [List company signatories](actions/list-company-signatories.md) | `GET /wep/companies/:companyId/signatories` | [docs](https://apidocs.worklio.com/reference/get_wep-companies-companyid-signatories) |
| [List company work locations](actions/list-company-work-locations.md) | `GET /wep/companies/:companyId/worklocations` | [docs](https://apidocs.worklio.com/docs/work-with-work-locations) |
| [Set company access policy](actions/set-company-access-policy.md) | `POST /wep/companies/:companyId/access-policy` | [docs](https://apidocs.worklio.com/reference/post_wep-companies-companyid-access-policy) |
| [Update company department](actions/update-company-department.md) | `PATCH /wep/companies/:companyId/departments/:departmentId` | [docs](https://apidocs.worklio.com/reference/patch_wep-companies-companyid-departments-departmentid) |
| [Update company position](actions/update-company-position.md) | `PATCH /wep/companies/:companyId/positions/:positionId` | [docs](https://apidocs.worklio.com/reference/patch_wep-companies-companyid-positions-positionid) |
