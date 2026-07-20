# Good Grants: Native API Reference

A consolidated summary of Good Grants's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.goodgrants.com
- **API base URL:** `https://api.cr4ce.com`

## Authentication

### API Key

Authenticate Good Grants using an API key generated in Settings > Integrations > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://apidocs.goodgrants.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.Creative Force.v2.3+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `per_page` in the query string to set the page size (accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create application](actions/create-application.md) | `POST application` | [docs](https://apidocs.goodgrants.com) |
| [Create field](actions/create-field.md) | `POST field` | [docs](https://apidocs.goodgrants.com) |
| [Create user](actions/create-user.md) | `POST user` | [docs](https://apidocs.goodgrants.com) |
| [Create webhook](actions/create-webhook.md) | `POST webhook` | [docs](https://apidocs.goodgrants.com) |
| [Delete application](actions/delete-application.md) | `DELETE application/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Delete user](actions/delete-user.md) | `DELETE user/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Delete webhook](actions/delete-webhook.md) | `DELETE webhook/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Get account](actions/get-account.md) | `GET account` | [docs](https://apidocs.goodgrants.com) |
| [Get application](actions/get-application.md) | `GET application/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Get form](actions/get-form.md) | `GET form/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Get user](actions/get-user.md) | `GET user/:identifier` | [docs](https://apidocs.goodgrants.com) |
| [Get webhook](actions/get-webhook.md) | `GET webhook/:slug` | [docs](https://apidocs.goodgrants.com) |
| [List applications](actions/list-applications.md) | `GET application` | [docs](https://apidocs.goodgrants.com) |
| [List categories](actions/list-categories.md) | `GET category` | [docs](https://apidocs.goodgrants.com) |
| [List chapters](actions/list-chapters.md) | `GET chapter` | [docs](https://apidocs.goodgrants.com) |
| [List fields](actions/list-fields.md) | `GET field` | [docs](https://apidocs.goodgrants.com) |
| [List forms](actions/list-forms.md) | `GET form` | [docs](https://apidocs.goodgrants.com) |
| [List grant statuses](actions/list-grant-statuses.md) | `GET grant-status` | [docs](https://apidocs.goodgrants.com) |
| [List seasons](actions/list-seasons.md) | `GET season` | [docs](https://apidocs.goodgrants.com) |
| [List users](actions/list-users.md) | `GET user` | [docs](https://apidocs.goodgrants.com) |
| [List webhooks](actions/list-webhooks.md) | `GET webhook` | [docs](https://apidocs.goodgrants.com) |
| [Update application](actions/update-application.md) | `PUT application/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Update user](actions/update-user.md) | `PUT user/:slug` | [docs](https://apidocs.goodgrants.com) |
| [Update webhook](actions/update-webhook.md) | `PUT webhook/:slug` | [docs](https://apidocs.goodgrants.com) |
