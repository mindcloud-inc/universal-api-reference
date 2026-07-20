# Action1: Native API Reference

A consolidated summary of Action1's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.action1.com/apidocs/
- **API base URL:** `https://app.action1.com/api/3.0`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://app.action1.com/api/3.0/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.action1.com/api/3.0/oauth2/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://www.action1.com/api-documentation/authentication/)

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `from` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Endpoint Status](actions/check-endpoint-status.md) | `GET /endpoints/status/:orgId` | [docs](https://app.action1.com/apidocs/#/Endpoints/endpoints_status) |
| [Get Current User Settings](actions/get-current-user-settings.md) | `GET /me` | [docs](https://app.action1.com/apidocs/#/Security.%20Users%20Management/me) |
| [Get Endpoint](actions/get-endpoint.md) | `GET /endpoints/managed/:orgId/:endpointId` | [docs](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed_endpointId) |
| [Get Endpoint Group](actions/get-endpoint-group.md) | `GET /endpoints/groups/:orgId/:groupId` | [docs](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_groupId) |
| [Get Missing Update](actions/get-missing-update.md) | `GET /updates/:orgId/:packageId` | [docs](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_packageId_get) |
| [Get Report Rows](actions/get-report-rows.md) | `GET /reportdata/:orgId/:reportId/data` | [docs](https://app.action1.com/apidocs/#/Reports.%20Report%20Data/reportdata_orgId_reportId_data_get) |
| [Get Vulnerability](actions/get-vulnerability.md) | `GET /vulnerabilities/:orgId/:cveId` | [docs](https://app.action1.com/apidocs/#/Vulnerability%20Management/vulnerabilities_orgId_cve_id_get) |
| [List Audit Events](actions/list-audit-events.md) | `GET /audit/events` | [docs](https://app.action1.com/apidocs/#/Audit%20Trail/audit_events_get) |
| [List Automation Instances](actions/list-automation-instances.md) | `GET /automations/instances/:orgId` | [docs](https://app.action1.com/apidocs/#/Automations.%20Instances/policies_instances_orgId_get) |
| [List Automation Schedules](actions/list-automation-schedules.md) | `GET /automations/schedules/:orgId` | [docs](https://app.action1.com/apidocs/#/Automations.%20Schedules/policies_schedules_orgId_get) |
| [List Endpoint Group Contents](actions/list-endpoint-group-contents.md) | `GET /endpoints/groups/:orgId/:groupId/contents` | [docs](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_groupId_contents_get) |
| [List Endpoint Groups](actions/list-endpoint-groups.md) | `GET /endpoints/groups/:orgId` | [docs](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_orgId) |
| [List Endpoint Installed Software Rows](actions/list-endpoint-installed-software-rows.md) | `GET /installed-software/:orgId/data/:endpointId` | [docs](https://app.action1.com/apidocs/#/Software%20Deployment.%20Installed%20Software%20Inventory/apps_orgId_data_endpointId_get) |
| [List Endpoint Missing Updates](actions/list-endpoint-missing-updates.md) | `GET /endpoints/managed/:orgId/:endpointId/missing-updates` | [docs](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed_endpointId_missing_updates) |
| [List Endpoints](actions/list-endpoints.md) | `GET /endpoints/managed/:orgId` | [docs](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed) |
| [List Installed Software Rows](actions/list-installed-software-rows.md) | `GET /installed-software/:orgId/data` | [docs](https://app.action1.com/apidocs/#/Software%20Deployment.%20Installed%20Software%20Inventory/apps_orgId_data_get) |
| [List Missing Update Version Endpoints](actions/list-missing-update-version-endpoints.md) | `GET /updates/:orgId/:packageId/versions/:versionId/endpoints` | [docs](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_packageId_versions_versionId_endpoints_get) |
| [List Missing Updates](actions/list-missing-updates.md) | `GET /updates/:orgId` | [docs](https://app.action1.com/apidocs/#/Software%20Deployment.%20Updates%20(Patches)/updates_orgId_get) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://app.action1.com/apidocs/#/Security.%20Organization%20Object/organizations_get) |
| [List Reports](actions/list-reports.md) | `GET /reports/all` | [docs](https://app.action1.com/apidocs/#/Reports.%20Report%20Definition%20Objects/reports_all_get) |
| [List Vulnerabilities](actions/list-vulnerabilities.md) | `GET /vulnerabilities/:orgId` | [docs](https://app.action1.com/apidocs/#/Vulnerability%20Management/vulnerabilities_orgId_get) |
| [List Vulnerability Endpoints](actions/list-vulnerability-endpoints.md) | `GET /vulnerabilities/:orgId/:cveId/endpoints` | [docs](https://app.action1.com/apidocs/#/Vulnerability%20Management/vulnerabilities_orgId_cve_id_endpoints_get) |
| [List Vulnerability Remediations](actions/list-vulnerability-remediations.md) | `GET /vulnerabilities/:orgId/:cveId/remediations` | [docs](https://app.action1.com/apidocs/#/Vulnerability%20Management/vulnerabilities_orgId_cve_id_remediations_get) |
| [Search](actions/search.md) | `GET /search/:orgId` | [docs](https://app.action1.com/apidocs/#/Search/search) |
