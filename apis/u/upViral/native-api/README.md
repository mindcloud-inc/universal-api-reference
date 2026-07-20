# UpViral: Native API Reference

A consolidated summary of UpViral's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://www.upviral.com/api
- **API base URL:** `https://app.upviral.com/api/v1/`

## Authentication

### API Key

Authenticate UpViral requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.upviral.com/support/solutions/articles/4000168687-where-can-i-find-my-upviral-api-key-)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `size` in the request body to set the page size (minimum 1). Use `start` in the request body as the record offset; numbering starts at 1.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [Add Contact Points](actions/add-contact-points.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [Get Contact](actions/get-contact.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [Get Contact By Email](actions/get-contact-by-email.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [List Campaigns](actions/list-campaigns.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [List Contacts](actions/list-contacts.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [List Contacts By Points](actions/list-contacts-by-points.md) | `POST /` | [docs](https://www.upviral.com/api) |
| [List Custom Fields](actions/list-custom-fields.md) | `POST /` | [docs](https://www.upviral.com/api) |
