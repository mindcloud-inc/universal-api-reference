# Documenso: Native API Reference

A consolidated summary of Documenso's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.documenso.com/docs/developers/api
- **API base URL:** `https://app.documenso.com/api/v2`

## Authentication

### API Token

Authenticate Documenso requests with a Documenso API token created from Settings > API Tokens.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.documenso.com/docs/developers/getting-started/authentication)

## Pagination

Use `perPage` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderByColumn` in the query string. Set the direction separately with `orderByDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /envelope/create` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [Create Document From Template](actions/create-document-from-template.md) | `POST /template/use` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
| [Create Fields](actions/create-fields.md) | `POST /envelope/field/create-many` | [docs](https://docs.documenso.com/docs/developers/api/fields) |
| [Create Recipients](actions/create-recipients.md) | `POST /envelope/recipient/create-many` | [docs](https://docs.documenso.com/docs/developers/api/recipients) |
| [Create Template](actions/create-template.md) | `POST /template/create` | [docs](https://docs.documenso.com/docs/developers/api/teams) |
| [Delete Document](actions/delete-document.md) | `POST /envelope/delete` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [Delete Field](actions/delete-field.md) | `POST /envelope/field/delete` | [docs](https://docs.documenso.com/docs/developers/api/fields) |
| [Delete Recipient](actions/delete-recipient.md) | `POST /envelope/recipient/delete` | [docs](https://docs.documenso.com/docs/developers/api/recipients) |
| [Delete Template](actions/delete-template.md) | `POST /template/delete` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
| [Duplicate Template](actions/duplicate-template.md) | `POST /template/duplicate` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
| [Get Document](actions/get-document.md) | `GET /envelope/:envelopeId` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [Get Field](actions/get-field.md) | `GET /envelope/field/:fieldId` | [docs](https://docs.documenso.com/docs/developers/api/fields) |
| [Get Recipient](actions/get-recipient.md) | `GET /envelope/recipient/:recipientId` | [docs](https://docs.documenso.com/docs/developers/api/recipients) |
| [Get Template](actions/get-template.md) | `GET /template/:templateId` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
| [List Documents](actions/list-documents.md) | `GET /envelope` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [List Templates](actions/list-templates.md) | `GET /template` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
| [Send Document](actions/send-document.md) | `POST /envelope/distribute` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [Update Document](actions/update-document.md) | `POST /envelope/update` | [docs](https://docs.documenso.com/docs/developers/api/documents) |
| [Update Recipients](actions/update-recipients.md) | `POST /envelope/recipient/update-many` | [docs](https://docs.documenso.com/docs/developers/api/recipients) |
| [Update Template](actions/update-template.md) | `POST /template/update` | [docs](https://docs.documenso.com/docs/developers/api/templates) |
