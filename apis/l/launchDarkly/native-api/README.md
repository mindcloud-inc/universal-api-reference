# LaunchDarkly: Native API Reference

A consolidated summary of LaunchDarkly's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://launchdarkly.com/docs/api
- **OpenAPI specification:** https://app.launchdarkly.com/api/v2/openapi.json
- **API base URL:** `https://app.launchdarkly.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://launchdarkly.com/docs/home/account/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Feature Flag](actions/copy-feature-flag.md) | `POST /flags/:projectKey/:featureFlagKey/copy` | [docs](https://launchdarkly.com/docs/api/feature-flags/copy-feature-flag) |
| [Create Feature Flag](actions/create-feature-flag.md) | `POST /flags/:projectKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/post-feature-flag) |
| [Create Segment](actions/create-segment.md) | `POST /segments/:projectKey/:environmentKey` | [docs](https://launchdarkly.com/docs/api/segments/post-segment) |
| [Delete Feature Flag](actions/delete-feature-flag.md) | `DELETE /flags/:projectKey/:featureFlagKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/delete-feature-flag) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:projectKey/:environmentKey/:segmentKey` | [docs](https://launchdarkly.com/docs/api/segments/delete-segment) |
| [Evaluate Flags](actions/evaluate-flags.md) | `POST /projects/:projectKey/environments/:environmentKey/flags/evaluate` | [docs](https://launchdarkly.com/docs/api/contexts/evaluate-context-instance) |
| [Get Context](actions/get-context.md) | `GET /projects/:projectKey/environments/:environmentKey/contexts/:kind/:key` | [docs](https://launchdarkly.com/docs/api/contexts/get-contexts) |
| [Get Environment](actions/get-environment.md) | `GET /projects/:projectKey/environments/:environmentKey` | [docs](https://launchdarkly.com/docs/api/environments/get-environment) |
| [Get Environment Flag Status](actions/get-environment-flag-status.md) | `GET /flag-statuses/:projectKey/:environmentKey/:featureFlagKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-status) |
| [Get Feature Flag](actions/get-feature-flag.md) | `GET /flags/:projectKey/:featureFlagKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag) |
| [Get Flag Status](actions/get-flag-status.md) | `GET /flag-status/:projectKey/:featureFlagKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-status-across-environments) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectKey` | [docs](https://launchdarkly.com/docs/api/projects/get-project) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:projectKey/:environmentKey/:segmentKey` | [docs](https://launchdarkly.com/docs/api/segments/get-segment) |
| [List Audit Log](actions/list-audit-log.md) | `GET /auditlog` | [docs](https://launchdarkly.com/docs/api/audit-log/get-audit-log-entries) |
| [List Environments](actions/list-environments.md) | `GET /projects/:projectKey/environments` | [docs](https://launchdarkly.com/docs/api/environments/get-environments-by-project) |
| [List Feature Flags](actions/list-feature-flags.md) | `GET /flags/:projectKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/get-feature-flags) |
| [List Flag Statuses](actions/list-flag-statuses.md) | `GET /flag-statuses/:projectKey/:environmentKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-statuses) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://launchdarkly.com/docs/api/account-members/get-members) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://launchdarkly.com/docs/api/projects/get-projects) |
| [List Segments](actions/list-segments.md) | `GET /segments/:projectKey/:environmentKey` | [docs](https://launchdarkly.com/docs/api/segments/get-segments) |
| [Search Contexts](actions/search-contexts.md) | `POST /projects/:projectKey/environments/:environmentKey/contexts/search` | [docs](https://launchdarkly.com/docs/api/contexts/search-contexts) |
| [Update Environment](actions/update-environment.md) | `PATCH /projects/:projectKey/environments/:environmentKey` | [docs](https://launchdarkly.com/docs/api/environments/patch-environment) |
| [Update Feature Flag](actions/update-feature-flag.md) | `PATCH /flags/:projectKey/:featureFlagKey` | [docs](https://launchdarkly.com/docs/api/feature-flags/patch-feature-flag) |
| [Update Segment](actions/update-segment.md) | `PATCH /segments/:projectKey/:environmentKey/:segmentKey` | [docs](https://launchdarkly.com/docs/api/segments/patch-segment) |
