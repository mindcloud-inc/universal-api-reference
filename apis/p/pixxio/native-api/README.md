# pixx.io: Native API Reference

A consolidated summary of pixx.io's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.pixxio.com/docs
- **OpenAPI specification:** https://api.pixxio.com/docs/openapi
- **API base URL:** `https://mindcloudpixx260413.px.media/api/v1`

## Authentication

### API Key

Authenticate with a pixx.io API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.pixxio.com/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 10000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://api.pixxio.com/docs/openapi) |
| [Create Direct Link](actions/create-direct-link.md) | `POST /directLinks` | [docs](https://api.pixxio.com/docs/openapi) |
| [Create External Share](actions/create-external-share.md) | `POST /externalShares` | [docs](https://api.pixxio.com/docs/openapi) |
| [Create Upload Link](actions/create-upload-link.md) | `POST /uploadLinks` | [docs](https://api.pixxio.com/docs/openapi) |
| [Download File](actions/download-file.md) | `GET /files/:id/convert` | [docs](https://api.pixxio.com/docs/openapi) |
| [Download Files](actions/download-files.md) | `GET /files/convert` | [docs](https://api.pixxio.com/docs/openapi) |
| [Download Keywords CSV](actions/download-keywords-csv.md) | `GET /keywords/csv` | [docs](https://api.pixxio.com/docs/openapi) |
| [Download Synonyms CSV](actions/download-synonyms-csv.md) | `GET /synonyms/csv` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Collection](actions/get-collection.md) | `GET /collections/:collection_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Current User](actions/get-current-user.md) | `GET /users/current` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Custom Metadata](actions/get-custom-metadata.md) | `GET /metadata/custom/:custom_metadata_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Direct Link](actions/get-direct-link.md) | `GET /directLinks/:id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Directory](actions/get-directory.md) | `GET /directories/:directory_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get External Share](actions/get-external-share.md) | `GET /externalShares/:id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get File](actions/get-file.md) | `GET /files/:id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get File State](actions/get-file-state.md) | `GET /fileStates/:file_state_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Permission Group](actions/get-permission-group.md) | `GET /permissionGroups/:permission_group_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Upload Link](actions/get-upload-link.md) | `GET /uploadLinks/:uploadlink_id` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get Upload Link Basic Info](actions/get-upload-link-basic-info.md) | `GET /uploadLinks/basicInfo` | [docs](https://api.pixxio.com/docs/openapi) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Custom Metadata](actions/list-custom-metadata.md) | `GET /metadata/custom` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Direct Links](actions/list-direct-links.md) | `GET /directLinks` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Directories](actions/list-directories.md) | `GET /directories` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Directory Tree](actions/list-directory-tree.md) | `GET /directories/tree` | [docs](https://api.pixxio.com/docs/openapi) |
| [List External Shares](actions/list-external-shares.md) | `GET /externalShares` | [docs](https://api.pixxio.com/docs/openapi) |
| [List File States](actions/list-file-states.md) | `GET /fileStates` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Important Metadata](actions/list-important-metadata.md) | `GET /metadata/important` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Internal Metadata](actions/list-internal-metadata.md) | `GET /metadata/internal` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Keywords](actions/list-keywords.md) | `GET /keywords` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Permission Groups](actions/list-permission-groups.md) | `GET /permissionGroups` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Portals](actions/list-portals.md) | `GET /portals` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Standard Metadata](actions/list-standard-metadata.md) | `GET /metadata/standard` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Synonym Columns](actions/list-synonym-columns.md) | `GET /synonymColumns` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Synonyms](actions/list-synonyms.md) | `GET /synonyms` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Upload Link Users](actions/list-upload-link-users.md) | `GET /uploadLinkUsers` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Upload Links](actions/list-upload-links.md) | `GET /uploadLinks` | [docs](https://api.pixxio.com/docs/openapi) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.pixxio.com/docs/openapi) |
