# Olostep: Native API Reference

A consolidated summary of Olostep's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.olostep.com/api-reference/common/object-oriented
- **API base URL:** `https://api.olostep.com`

## Authentication

### API Key

Connect using your Olostep API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.olostep.com/get-started/authentication)

### Bearer Token

Connect using your Olostep API token. MindCloud will send it as an Authorization bearer token.

### Credentials

- **API Token:** `apiKey` · required · Paste your raw Olostep API token. MindCloud will send it as `Authorization: Bearer <API-TOKEN>`.

[Official authentication documentation](https://docs.olostep.com/get-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `schedules`.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete File Upload](actions/complete-file-upload.md) | `POST /v1/files/[:file_id]/complete` | [docs](https://docs.olostep.com/api-reference/files/complete) |
| [Create Answer](actions/create-answer.md) | `POST /v1/answers` | [docs](https://docs.olostep.com/api-reference/answers/create) |
| [Create Batch](actions/create-batch.md) | `POST /v1/batches` | [docs](https://docs.olostep.com/api-reference/batches/create) |
| [Create Crawl](actions/create-crawl.md) | `POST /v1/crawls` | [docs](https://docs.olostep.com/api-reference/crawls/create) |
| [Create File Upload](actions/create-file-upload.md) | `POST /v1/files` | [docs](https://docs.olostep.com/api-reference/files/create) |
| [Create Map](actions/create-map.md) | `POST /v1/maps` | [docs](https://docs.olostep.com/api-reference/maps/create) |
| [Create Schedule](actions/create-schedule.md) | `POST /v1/schedules` | [docs](https://docs.olostep.com/api-reference/schedules/create) |
| [Create Scrape](actions/create-scrape.md) | `POST /v1/scrapes` | [docs](https://docs.olostep.com/api-reference/scrapes/create) |
| [Create Search](actions/create-search.md) | `POST /v1/searches` | [docs](https://docs.olostep.com/api-reference/searches/create) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/[:file_id]` | [docs](https://docs.olostep.com/api-reference/files/delete) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /v1/schedules/[:schedule_id]` | [docs](https://docs.olostep.com/api-reference/schedules/delete) |
| [Get Answer](actions/get-answer.md) | `GET /v1/answers/[:answer_id]` | [docs](https://docs.olostep.com/api-reference/answers/get) |
| [Get Batch](actions/get-batch.md) | `GET /v1/batches/[:batch_id]` | [docs](https://docs.olostep.com/api-reference/batches/info) |
| [Get Crawl](actions/get-crawl.md) | `GET /v1/crawls/[:crawl_id]` | [docs](https://docs.olostep.com/api-reference/crawls/info) |
| [Get File](actions/get-file.md) | `GET /v1/files/[:file_id]` | [docs](https://docs.olostep.com/api-reference/files/get) |
| [Get Map](actions/get-map.md) | `GET /v1/maps/[:map_id]` | [docs](https://docs.olostep.com/api-reference/maps/get) |
| [Get Schedule](actions/get-schedule.md) | `GET /v1/schedules/[:schedule_id]` | [docs](https://docs.olostep.com/api-reference/schedules/get) |
| [Get Scrape](actions/get-scrape.md) | `GET /v1/scrapes/[:scrape_id]` | [docs](https://docs.olostep.com/api-reference/scrapes/get) |
| [Get Search](actions/get-search.md) | `GET /v1/searches/[:search_id]` | [docs](https://docs.olostep.com/api-reference/searches/get) |
| [List Batch Items](actions/list-batch-items.md) | `GET /v1/batches/[:batch_id]/items` | [docs](https://docs.olostep.com/api-reference/batches/items) |
| [List Crawl Pages](actions/list-crawl-pages.md) | `GET /v1/crawls/[:crawl_id]/pages` | [docs](https://docs.olostep.com/api-reference/crawls/pages) |
| [List Schedules](actions/list-schedules.md) | `GET /v1/schedules` | [docs](https://docs.olostep.com/api-reference/schedules/list) |
| [Retrieve Content](actions/retrieve-content.md) | `GET /v1/retrieve` | [docs](https://docs.olostep.com/api-reference/retrieve) |
