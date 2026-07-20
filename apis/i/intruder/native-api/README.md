# Intruder: Native API Reference

A consolidated summary of Intruder's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developers.intruder.io/reference
- **API base URL:** `https://api.intruder.io/v1`

## Authentication

### API Key

Authenticate with an Intruder personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.intruder.io/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Target](actions/add-target.md) | `POST /targets/` | [docs](https://developers.intruder.io/reference/targets_create-1) |
| [Add Target API Schema](actions/add-target-api-schema.md) | `POST /targets/:target_id/api_schemas/` | [docs](https://developers.intruder.io/reference/targets_api_schemas_create) |
| [Add Target Authentication](actions/add-target-authentication.md) | `POST /targets/:target_id/authentications/` | [docs](https://developers.intruder.io/reference/targets_authentications_create) |
| [Bulk Add Targets](actions/bulk-add-targets.md) | `POST /targets/bulk/` | [docs](https://developers.intruder.io/reference/targets_bulk_create) |
| [Cancel Scan](actions/cancel-scan.md) | `POST /scans/:id/cancel/` | [docs](https://developers.intruder.io/reference/scans_cancel_create) |
| [Check Health](actions/check-health.md) | `GET /health/` | [docs](https://developers.intruder.io/reference/health_list-1) |
| [Create Scan Schedule](actions/create-scan-schedule.md) | `POST /scans/schedules/` | [docs](https://developers.intruder.io/reference/scans_schedules_create) |
| [Delete Scan Schedule](actions/delete-scan-schedule.md) | `DELETE /scans/schedules/:id/` | [docs](https://developers.intruder.io/reference/scans_schedules_destroy) |
| [Delete Target](actions/delete-target.md) | `DELETE /targets/:id/` | [docs](https://developers.intruder.io/reference/targets_destroy) |
| [Delete Target API Schema](actions/delete-target-api-schema.md) | `DELETE /targets/:target_id/api_schemas/:id/` | [docs](https://developers.intruder.io/reference/targets_api_schemas_destroy) |
| [Delete Target Authentication](actions/delete-target-authentication.md) | `DELETE /targets/:target_id/authentications/:id/` | [docs](https://developers.intruder.io/reference/targets_authentications_destroy) |
| [Delete Target Tag](actions/delete-target-tag.md) | `DELETE /targets/:target_id/tags/:name/` | [docs](https://developers.intruder.io/reference/targets_tags_destroy) |
| [List Issue Occurrences](actions/list-issue-occurrences.md) | `GET /issues/:issueId/occurrences/` | [docs](https://developers.intruder.io/reference/issues_occurrences_list-1) |
| [List Issues](actions/list-issues.md) | `GET /issues/` | [docs](https://developers.intruder.io/reference/issues_list-1) |
| [List Licenses](actions/list-licenses.md) | `GET /licenses/` | [docs](https://developers.intruder.io/reference/licenses_list) |
| [List Occurrence Scanner Output](actions/list-occurrence-scanner-output.md) | `GET /issues/:issue_id/occurrences/:occurrence_id/scanner_output/` | [docs](https://developers.intruder.io/reference/issues_occurrences_scanner_output_list) |
| [List Scan Schedules](actions/list-scan-schedules.md) | `GET /scans/schedules/` | [docs](https://developers.intruder.io/reference/scans_schedules_list) |
| [List Scans](actions/list-scans.md) | `GET /scans/` | [docs](https://developers.intruder.io/reference/scans_list-1) |
| [List Target API Schemas](actions/list-target-api-schemas.md) | `GET /targets/:target_id/api_schemas/` | [docs](https://developers.intruder.io/reference/targets_api_schemas_list) |
| [List Target Authentications](actions/list-target-authentications.md) | `GET /targets/:target_id/authentications/` | [docs](https://developers.intruder.io/reference/targets_authentications_list) |
| [List Targets](actions/list-targets.md) | `GET /targets/` | [docs](https://developers.intruder.io/reference/targets_list-1) |
| [Retrieve Scan Details](actions/retrieve-scan-details.md) | `GET /scans/:id/` | [docs](https://developers.intruder.io/reference/scans_retrieve) |
| [Snooze Issue](actions/snooze-issue.md) | `POST /issues/:id/snooze/` | [docs](https://developers.intruder.io/reference/issues_snooze_create) |
| [Snooze Issue Occurrence](actions/snooze-issue-occurrence.md) | `POST /issues/:issueId/occurrences/:id/snooze/` | [docs](https://developers.intruder.io/reference/issues_occurrences_snooze_create) |
| [Start Scan](actions/start-scan.md) | `POST /scans/` | [docs](https://developers.intruder.io/reference/scans_create-1) |
| [Update Scan Schedule](actions/update-scan-schedule.md) | `PATCH /scans/schedules/:id/` | [docs](https://developers.intruder.io/reference/scans_schedules_partial_update) |
| [Update Target API Schema](actions/update-target-api-schema.md) | `PATCH /targets/:target_id/api_schemas/:id/` | [docs](https://developers.intruder.io/reference/targets_api_schemas_partial_update) |
| [Update Target Authentication](actions/update-target-authentication.md) | `PATCH /targets/:target_id/authentications/:id/` | [docs](https://developers.intruder.io/reference/targets_authentications_partial_update) |
