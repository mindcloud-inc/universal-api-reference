# Refiner: Native API Reference

A consolidated summary of Refiner's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://refiner.io/docs/api/
- **API base URL:** `https://api.refiner.io/v1`

## Authentication

### API Key

Connect with a Refiner REST API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://refiner.io/docs/api/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `input.pagination.next_page_cursor`. The total page count is read from `input.pagination.last_page`. The current page number is read from `input.pagination.current_page`.

## Pagination

Use `page_length` in the query string to set the page size (default 50; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User to Segment](actions/add-user-to-segment.md) | `POST /sync-segment` | [docs](https://refiner.io/docs/api/#link-users) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact` | [docs](https://refiner.io/docs/api/#delete-contact) |
| [Delete Form](actions/delete-form.md) | `DELETE /forms` | [docs](https://refiner.io/docs/api/#delete-form) |
| [Duplicate Form](actions/duplicate-form.md) | `POST /forms/duplicate` | [docs](https://refiner.io/docs/api/#duplicate-form) |
| [Get Account Info](actions/get-account-info.md) | `GET /account` | [docs](https://refiner.io/docs/api/#get-account-info) |
| [Get Contact](actions/get-contact.md) | `GET /contact` | [docs](https://refiner.io/docs/api/#get-contact) |
| [Get Reporting](actions/get-reporting.md) | `GET /reporting` | [docs](https://refiner.io/docs/api/#get-reporting) |
| [Identify User](actions/identify-user.md) | `POST /identify-user` | [docs](https://refiner.io/docs/api/#identify-user) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://refiner.io/docs/api/#get-contacts) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://refiner.io/docs/api/#get-forms) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://refiner.io/docs/api/#get-responses) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://refiner.io/docs/api/#get-segments) |
| [Publish Form](actions/publish-form.md) | `POST /forms/publish` | [docs](https://refiner.io/docs/api/#publish-form) |
| [Remove User from Segment](actions/remove-user-from-segment.md) | `DELETE /sync-segment` | [docs](https://refiner.io/docs/api/#link-users) |
| [Store Responses](actions/store-responses.md) | `POST /responses` | [docs](https://refiner.io/docs/api/#store-responses) |
| [Tag Responses](actions/tag-responses.md) | `POST /responses/tags` | [docs](https://refiner.io/docs/api/#tag-responses) |
| [Track Event](actions/track-event.md) | `POST /track-event` | [docs](https://refiner.io/docs/api/#track-event) |
