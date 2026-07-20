# SeekTable: Native API Reference

A consolidated summary of SeekTable's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.seektable.com/help/web-api-integration
- **OpenAPI specification:** https://www.seektable.com/PowerAutomate_SeekTable.openapi.json
- **API base URL:** `https://www.seektable.com`

## Authentication

### API Key

Use a SeekTable API key from Manage Account -> Get API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.seektable.com/help/ms-flow-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | `POST /api/account/:id/team/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Add Users To Team Group](actions/add-users-to-team-group.md) | `POST /api/account/:id/team/group/:group_id/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Assign Groups For Team Members](actions/assign-groups-for-team-members.md) | `POST /api/account/:id/team/member/assigngroups` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Backup Account Data](actions/backup-account-data.md) | `GET /api/account/backup` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Create Team Group](actions/create-team-group.md) | `POST /api/account/:id/team/group` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Create User Account](actions/create-user-account.md) | `POST /api/account` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Delete Team Group](actions/delete-team-group.md) | `DELETE /api/account/:id/team/group/:group_id` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Delete User Account](actions/delete-user-account.md) | `DELETE /api/account/:id` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Export Dashboard](actions/export-dashboard.md) | `GET /api/dashboard/:dashboard_id/export` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Export Report](actions/export-report.md) | `GET /api/report/:report_id/export` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Get Cube Info](actions/get-cube-info.md) | `GET /api/cube/:cube_id` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Get Report Info](actions/get-report-info.md) | `GET /api/report/:report_id` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Get User Account](actions/get-user-account.md) | `GET /api/account/:id` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [List Cubes](actions/list-cubes.md) | `GET /api/cube` | [docs](https://www.seektable.com/help/web-api-integration) |
| [List Dashboards](actions/list-dashboards.md) | `GET /api/dashboard` | [docs](https://www.seektable.com/help/web-api-integration) |
| [List Reports](actions/list-reports.md) | `GET /api/report` | [docs](https://www.seektable.com/help/web-api-integration) |
| [List Team Group Members](actions/list-team-group-members.md) | `GET /api/account/:id/team/group/:group_id/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [List Team Groups](actions/list-team-groups.md) | `GET /api/account/:id/team/group` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [List Team Members](actions/list-team-members.md) | `GET /api/account/:id/team/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [List User Accounts](actions/list-user-accounts.md) | `GET /api/account` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Remove Team Members](actions/remove-team-members.md) | `DELETE /api/account/:id/team/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Remove Users From Team Group](actions/remove-users-from-team-group.md) | `DELETE /api/account/:id/team/group/:group_id/member` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Share Report By Email](actions/share-report-by-email.md) | `POST /api/report/:report_id/share/email` | [docs](https://www.seektable.com/help/web-api-integration) |
| [Update User Account](actions/update-user-account.md) | `PUT /api/account/:id` | [docs](https://www.seektable.com/help/self-hosted-admin-accounts-api) |
| [Upload CSV File](actions/upload-csv-file.md) | `POST /api/cube/import/csv` | [docs](https://www.seektable.com/help/web-api-integration) |
