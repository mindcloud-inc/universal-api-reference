# Zoho Analytics: Native API Reference

A consolidated summary of Zoho Analytics's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/analytics/api/v2/introduction.html
- **API base URL:** `https://analyticsapi.zoho.com/restapi/v2`

## Authentication

### OAuth 2.0

### Credentials

- **Analytics Server URL:** `analyticsServerUrl` · required · Zoho Analytics API server URL for your data center. Use the exact server URI from Zoho's Server URI table, such as https://analyticsapi.zoho.com or https://analyticsapi.zoho.eu.
- **Organization ID:** `organizationId` · optional · Optional default Zoho Analytics organization ID. Run Get Organizations after connecting to find it, then save the organization you use most often.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoAnalytics.metadata.all ZohoAnalytics.data.all ZohoAnalytics.modeling.all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/analytics/api/v2/authentication.html)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Row](actions/add-row.md) | `POST /workspaces/[:workspace-id]/views/[:view-id]/rows` | [docs](https://www.zoho.com/analytics/api/v2/data-api/add-row.html) |
| [Create Export Job From SQL](actions/create-export-job-from-sql.md) | `GET /bulk/workspaces/[:workspace-id]/data` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/create-export/sql-query.html) |
| [Create Import Job For Existing Table](actions/create-import-job-for-existing-table.md) | `POST /bulk/workspaces/[:workspace-id]/views/[:view-id]/data` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/import-data-async/create-import-job/existing-table.html) |
| [Create Query Table](actions/create-query-table.md) | `POST /workspaces/[:workspace-id]/querytables` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/create-query-table.html) |
| [Create Report](actions/create-report.md) | `POST /workspaces/[:workspace-id]/reports` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/create-report.html) |
| [Create Table](actions/create-table.md) | `POST /workspaces/[:workspace-id]/tables` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/create-table.html) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/create-workspace.html) |
| [Delete Rows](actions/delete-rows.md) | `DELETE /workspaces/[:workspace-id]/views/[:view-id]/rows` | [docs](https://www.zoho.com/analytics/api/v2/data-api/delete-row.html) |
| [Delete View](actions/delete-view.md) | `DELETE /workspaces/[:workspace-id]/views/[:view-id]` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/delete-view.html) |
| [Download Exported Data](actions/download-exported-data.md) | `GET /bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]/data` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/download-export.html) |
| [Export View Data](actions/export-view-data.md) | `GET /workspaces/[:workspace-id]/views/[:view-id]/data` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/export-data.html) |
| [Get Export Job Details](actions/get-export-job-details.md) | `GET /bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/get-export.html) |
| [Get Import Job Details](actions/get-import-job-details.md) | `GET /bulk/workspaces/[:workspace-id]/importjobs/[:job-id]` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/import-data-async/get-import-job.html) |
| [Get Meta Details](actions/get-meta-details.md) | `GET /metadetails` | [docs](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json) |
| [Get View](actions/get-view.md) | `GET /views/[:view-id]` | [docs](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/[:workspace-id]` | [docs](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json) |
| [Import Data Into Existing Table](actions/import-data-into-existing-table.md) | `POST /workspaces/[:workspace-id]/views/[:view-id]/data` | [docs](https://www.zoho.com/analytics/api/v2/bulk-api/import-data/existing-table.html) |
| [List Folders](actions/list-folders.md) | `GET /workspaces/[:workspace-id]/folders` | [docs](https://www.zoho.com/analytics/api/v2/metadata-api/get-folders.html) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://www.zoho.com/analytics/api/v2/metadata-api/get-org.html) |
| [List Recent Views](actions/list-recent-views.md) | `GET /recentviews` | [docs](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json) |
| [List Views](actions/list-views.md) | `GET /workspaces/[:workspace-id]/views` | [docs](https://www.zoho.com/analytics/api/v2/metadata-api/get-views.html) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://raw.githubusercontent.com/zoho/analytics-oas/main/v2.0/metadata-api.json) |
| [Rename View](actions/rename-view.md) | `PUT /workspaces/[:workspace-id]/views/[:view-id]` | [docs](https://www.zoho.com/analytics/api/v2/modeling-api/rename-view.html) |
| [Update Rows](actions/update-rows.md) | `PUT /workspaces/[:workspace-id]/views/[:view-id]/rows` | [docs](https://www.zoho.com/analytics/api/v2/data-api/update-row.html) |
