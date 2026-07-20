# Intelliprint: Native API Reference

A consolidated summary of Intelliprint's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.intelliprint.net/api
- **OpenAPI specification:** https://registry.scalar.com/@intelliprint/apis/intelliprint-api-reference?format=json
- **API base URL:** `https://api.intelliprint.net/v1`

## Authentication

### API Key

Use your Intelliprint API key from the account dashboard. Runtime sends it as Authorization: Bearer <api key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.intelliprint.net/api)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort_field` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Background](actions/create-background.md) | `POST /backgrounds` | [docs](https://docs.intelliprint.net/api) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST /mailing_lists` | [docs](https://docs.intelliprint.net/api) |
| [Create Mailing List Recipient](actions/create-mailing-list-recipient.md) | `POST /mailing_lists/:mailingList/recipients` | [docs](https://docs.intelliprint.net/api) |
| [Create Print Job](actions/create-print-job.md) | `POST /prints` | [docs](https://docs.intelliprint.net/api) |
| [Delete Background](actions/delete-background.md) | `DELETE /backgrounds/:id` | [docs](https://docs.intelliprint.net/api) |
| [Delete Mailing List](actions/delete-mailing-list.md) | `DELETE /mailing_lists/:id` | [docs](https://docs.intelliprint.net/api) |
| [Delete Mailing List Recipient](actions/delete-mailing-list-recipient.md) | `DELETE /mailing_lists/:mailingList/recipients/:id` | [docs](https://docs.intelliprint.net/api) |
| [Delete Print Job](actions/delete-print-job.md) | `DELETE /prints/:id` | [docs](https://docs.intelliprint.net/api) |
| [List Backgrounds](actions/list-backgrounds.md) | `GET /backgrounds` | [docs](https://docs.intelliprint.net/api) |
| [List Mailing List Recipients](actions/list-mailing-list-recipients.md) | `GET /mailing_lists/:mailingList/recipients` | [docs](https://docs.intelliprint.net/api) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /mailing_lists` | [docs](https://docs.intelliprint.net/api) |
| [List Print Jobs](actions/list-print-jobs.md) | `GET /prints` | [docs](https://docs.intelliprint.net/api) |
| [Retrieve Background](actions/retrieve-background.md) | `GET /backgrounds/:id` | [docs](https://docs.intelliprint.net/api) |
| [Retrieve Mailing List](actions/retrieve-mailing-list.md) | `GET /mailing_lists/:id` | [docs](https://docs.intelliprint.net/api) |
| [Retrieve Mailing List Recipient](actions/retrieve-mailing-list-recipient.md) | `GET /mailing_lists/:mailingList/recipients/:id` | [docs](https://docs.intelliprint.net/api) |
| [Retrieve Print Job](actions/retrieve-print-job.md) | `GET /prints/:id` | [docs](https://docs.intelliprint.net/api) |
| [Update Background](actions/update-background.md) | `POST /backgrounds/:id` | [docs](https://docs.intelliprint.net/api) |
| [Update Mailing List](actions/update-mailing-list.md) | `POST /mailing_lists/:id` | [docs](https://docs.intelliprint.net/api) |
| [Update Mailing List Recipient](actions/update-mailing-list-recipient.md) | `POST /mailing_lists/:mailingList/recipients/:id` | [docs](https://docs.intelliprint.net/api) |
| [Update Print Job](actions/update-print-job.md) | `POST /prints/:id` | [docs](https://docs.intelliprint.net/api) |
