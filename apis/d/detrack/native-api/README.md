# Detrack: Native API Reference

A consolidated summary of Detrack's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://detrackapiv2.docs.apiary.io/
- **API base URL:** `https://app.detrack.com/api/v2`

## Authentication

### API Key

Connect Detrack with an API key from Integrations > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://help.detrack.com/en/articles/10773545-where-to-obtain-the-api-key-for-performing-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Create Jobs](actions/batch-create-jobs.md) | `POST /dn/jobs/bulk` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-create/create) |
| [Batch Delete Jobs](actions/batch-delete-jobs.md) | `DELETE /dn/jobs` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-update-delete/delete) |
| [Batch Update Jobs](actions/batch-update-jobs.md) | `PUT /dn/jobs` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/batch-update-delete/update) |
| [Bulk Create Depots](actions/bulk-create-depots.md) | `POST /dn/depots/bulk` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/bulk-create-depots/bulk-create) |
| [Bulk Delete Depots](actions/bulk-delete-depots.md) | `DELETE /dn/depots` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/bulk-delete) |
| [Bulk Update Depots](actions/bulk-update-depots.md) | `PUT /dn/depots` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/bulk-update) |
| [Create Depot](actions/create-depot.md) | `POST /dn/depots` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/create) |
| [Create Job](actions/create-job.md) | `POST /dn/jobs` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/list-create/create) |
| [Delete Job By D.O. Number](actions/delete-job-by-do-number.md) | `DELETE /dn/jobs/:do_number` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/delete) |
| [Delete Job By D.O. Number And Date](actions/delete-job-by-do-number-and-date.md) | `DELETE /dn/jobs/:do_number/:date` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do-and-date/delete) |
| [Export Job By D.O. Number](actions/export-job-by-do-number.md) | `GET /dn/jobs/export/:do_number` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/export-by-do/download-exported-file) |
| [Export Job By D.O. Number And Date](actions/export-job-by-do-number-and-date.md) | `GET /dn/jobs/export/:do_number/:date` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/export-by-do-and-date/download-exported-file) |
| [List Depots](actions/list-depots.md) | `GET /dn/depots` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/list-depots/list) |
| [List Depots By Name](actions/list-depots-by-name.md) | `GET /dn/depots` | [docs](https://detrackapiv2.docs.apiary.io/#reference/depots/retrieve-depot-by-name/show) |
| [List Jobs](actions/list-jobs.md) | `GET /dn/jobs` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/list-create/list) |
| [List Routes By Date](actions/list-routes-by-date.md) | `GET /dn/routes` | [docs](https://detrackapiv2.docs.apiary.io/#reference/routes/retrieve-routes-by-date/list) |
| [List Routes By Name](actions/list-routes-by-name.md) | `GET /dn/routes` | [docs](https://detrackapiv2.docs.apiary.io/#reference/routes/retrieve-route-by-name/list) |
| [Reattempt Job](actions/reattempt-job.md) | `POST /dn/jobs/reattempt` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/reattempt/reattempt) |
| [Retrieve Job By D.O. Number](actions/retrieve-job-by-do-number.md) | `GET /dn/jobs/:do_number` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/retrieve) |
| [Retrieve Job By D.O. Number And Date](actions/retrieve-job-by-do-number-and-date.md) | `GET /dn/jobs/:do_number/:date` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do-and-date/retrieve) |
| [Search Jobs](actions/search-jobs.md) | `POST /dn/jobs/search` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/search/search) |
| [Update Job By D.O. Number](actions/update-job-by-do-number.md) | `PUT /dn/jobs/:do_number` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do/update) |
| [Update Job By D.O. Number And Date](actions/update-job-by-do-number-and-date.md) | `PUT /dn/jobs/:do_number/:date` | [docs](https://detrackapiv2.docs.apiary.io/#reference/jobs/retrieve-update-delete-by-do-and-date/update) |
