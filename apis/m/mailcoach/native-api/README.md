# Mailcoach: Native API Reference

A consolidated summary of Mailcoach's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.mailcoach.app/api-documentation/
- **API base URL:** `https://mindcloud.mailcoach.app/api`

## Authentication

### API Token

Authenticate with a Mailcoach API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.mailcoach.app/api-documentation/introduction/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags To Subscriber](actions/add-tags-to-subscriber.md) | `POST /subscribers/:uuid/tags` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Confirm Subscriber](actions/confirm-subscriber.md) | `POST /subscribers/:uuid/confirm` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Create Email List](actions/create-email-list.md) | `POST /email-lists` | [docs](https://www.mailcoach.app/api-documentation/endpoints/email-lists/) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /email-lists/:emailListUuid/subscribers` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://www.mailcoach.app/api-documentation/endpoints/templates/) |
| [Delete Email List](actions/delete-email-list.md) | `DELETE /email-lists/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/email-lists/) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/templates/) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://www.mailcoach.app/api-documentation/introduction/authentication/) |
| [Get Email List](actions/get-email-list.md) | `GET /email-lists/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/email-lists/) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Get Template](actions/get-template.md) | `GET /templates/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/templates/) |
| [List Email Lists](actions/list-email-lists.md) | `GET /email-lists` | [docs](https://www.mailcoach.app/api-documentation/endpoints/email-lists/) |
| [List Subscribers](actions/list-subscribers.md) | `GET /email-lists/:emailListUuid/subscribers` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://www.mailcoach.app/api-documentation/endpoints/templates/) |
| [Remove Tags From Subscriber](actions/remove-tags-from-subscriber.md) | `DELETE /subscribers/:uuid/tags` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /subscribers/:uuid/unsubscribe` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Update Email List](actions/update-email-list.md) | `PUT /email-lists/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/email-lists/) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/subscribers/) |
| [Update Template](actions/update-template.md) | `PUT /templates/:uuid` | [docs](https://www.mailcoach.app/api-documentation/endpoints/templates/) |
