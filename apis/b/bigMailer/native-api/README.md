# BigMailer: Native API Reference

A consolidated summary of BigMailer's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.bigmailer.io/reference
- **API base URL:** `https://api.bigmailer.io/v1`

## Authentication

### API Key

Use a BigMailer API key from the API key management page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.bigmailer.io/docs/getting-started-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /brands/:brand_id/contacts` | [docs](https://docs.bigmailer.io/reference/createcontact) |
| [Create Field](actions/create-field.md) | `POST /brands/:brand_id/fields` | [docs](https://docs.bigmailer.io/reference/createfield) |
| [Create List](actions/create-list.md) | `POST /brands/:brand_id/lists` | [docs](https://docs.bigmailer.io/reference/createlist) |
| [Create or Update Contact](actions/create-or-update-contact.md) | `POST /brands/:brand_id/contacts/upsert` | [docs](https://docs.bigmailer.io/reference/upsertcontact) |
| [Create Template](actions/create-template.md) | `POST /brands/:brand_id/templates` | [docs](https://docs.bigmailer.io/reference/createtemplate) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /brands/:brand_id/contacts/:contact_id` | [docs](https://docs.bigmailer.io/reference/deletecontact) |
| [Delete Field](actions/delete-field.md) | `DELETE /brands/:brand_id/fields/:field_id` | [docs](https://docs.bigmailer.io/reference/deletefield) |
| [Delete List](actions/delete-list.md) | `DELETE /brands/:brand_id/lists/:list_id` | [docs](https://docs.bigmailer.io/reference/deletelist) |
| [Get Brand](actions/get-brand.md) | `GET /brands/:brand_id` | [docs](https://docs.bigmailer.io/reference/getbrand) |
| [Get Contact](actions/get-contact.md) | `GET /brands/:brand_id/contacts/:contact_id` | [docs](https://docs.bigmailer.io/reference/getcontact) |
| [Get Contact Batch Status](actions/get-contact-batch-status.md) | `GET /brands/:brand_id/contacts/batches/:batch_id` | [docs](https://docs.bigmailer.io/reference/getcontactbatch) |
| [Get Field](actions/get-field.md) | `GET /brands/:brand_id/fields/:field_id` | [docs](https://docs.bigmailer.io/reference/getfield) |
| [Get List](actions/get-list.md) | `GET /brands/:brand_id/lists/:list_id` | [docs](https://docs.bigmailer.io/reference/getlist) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://docs.bigmailer.io/reference/listbrands) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://docs.bigmailer.io/reference/listconnections) |
| [List Contacts](actions/list-contacts.md) | `GET /brands/:brand_id/contacts` | [docs](https://docs.bigmailer.io/reference/listcontacts) |
| [List Fields](actions/list-fields.md) | `GET /brands/:brand_id/fields` | [docs](https://docs.bigmailer.io/reference/listfields) |
| [List Lists](actions/list-lists.md) | `GET /brands/:brand_id/lists` | [docs](https://docs.bigmailer.io/reference/listlists) |
| [List Templates](actions/list-templates.md) | `GET /brands/:brand_id/templates` | [docs](https://docs.bigmailer.io/reference/listtemplates) |
| [Update Brand](actions/update-brand.md) | `POST /brands/:brand_id` | [docs](https://docs.bigmailer.io/reference/updatebrand) |
| [Update Contact](actions/update-contact.md) | `POST /brands/:brand_id/contacts/:contact_id` | [docs](https://docs.bigmailer.io/reference/updatecontact) |
| [Update Field](actions/update-field.md) | `POST /brands/:brand_id/fields/:field_id` | [docs](https://docs.bigmailer.io/reference/updatefield) |
| [Update List](actions/update-list.md) | `POST /brands/:brand_id/lists/:list_id` | [docs](https://docs.bigmailer.io/reference/updatelist) |
| [Upload Contact Batch](actions/upload-contact-batch.md) | `POST /brands/:brand_id/contacts/batches` | [docs](https://docs.bigmailer.io/reference/createcontactbatch) |
