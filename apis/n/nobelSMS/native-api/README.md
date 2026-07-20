# NobelSMS: Native API Reference

A consolidated summary of NobelSMS's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.nobelsms.com/
- **OpenAPI specification:** https://api.nobelsms.com/rest/swagger.json
- **API base URL:** `https://api.nobelsms.com/rest`

## Authentication

### JWT Token

Use a NobelSMS JWT token for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.nobelsms.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `rec_count` in the query string to set the page size. Use `first_rec` in the query string as the record offset; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Blacklist Entry](actions/create-blacklist-entry.md) | `POST /black_list` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Create Contact](actions/create-contact.md) | `POST /contact` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Create SMS Template](actions/create-sms-template.md) | `POST /sms_template` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Create Tag](actions/create-tag.md) | `POST /tag` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Delete Blacklist Entry](actions/delete-blacklist-entry.md) | `DELETE /black_list/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Delete SMS Template](actions/delete-sms-template.md) | `DELETE /sms_template/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tag/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Get Balance](actions/get-balance.md) | `GET /balance/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Get SMS Template](actions/get-sms-template.md) | `GET /sms_template/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Get Tag](actions/get-tag.md) | `GET /tag/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [List Balances](actions/list-balances.md) | `GET /balance` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | `GET /black_list` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [List Contacts](actions/list-contacts.md) | `GET /contact` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [List SMS Templates](actions/list-sms-templates.md) | `GET /sms_template` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [List Tags](actions/list-tags.md) | `GET /tag` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Update SMS Template](actions/update-sms-template.md) | `PUT /sms_template/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
| [Update Tag](actions/update-tag.md) | `PUT /tag/:id` | [docs](https://api.nobelsms.com/rest/swagger.json) |
