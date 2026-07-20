# ContactDrive: Native API Reference

A consolidated summary of ContactDrive's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://help.contactdrive.io/article/16-api-v1
- **API base URL:** `https://api.contactdrive.app/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.contactdrive.io/article/16-api-v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /contacts` | [docs](https://help.contactdrive.io/article/16-api-v1) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts` | [docs](https://help.contactdrive.io/article/16-api-v1) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://help.contactdrive.io/article/16-api-v1) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts` | [docs](https://help.contactdrive.io/article/16-api-v1) |
