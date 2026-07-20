# Ugosign: Native API Reference

A consolidated summary of Ugosign's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.ugosign.com/api/docs
- **API base URL:** `https://app.ugosign.com/api`

## Authentication

### API Key

Use a Ugosign API key with Bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.ugosign.com/help-center/article/generate-api-key-ugosign?lang=en)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://app.ugosign.com/api/docs) |
| [Create Contract](actions/create-contract.md) | `POST /v1/contracts` | [docs](https://app.ugosign.com/api/docs) |
| [Create Envelope](actions/create-envelope.md) | `POST /v1/envelopes` | [docs](https://app.ugosign.com/api/docs) |
| [Create Folder](actions/create-folder.md) | `POST /v1/folders` | [docs](https://app.ugosign.com/api/docs) |
| [Create Quick Envelope](actions/create-quick-envelope.md) | `POST /v1/envelopes/quick` | [docs](https://app.ugosign.com/api/docs) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/:contact` | [docs](https://app.ugosign.com/api/docs) |
| [Delete Contract](actions/delete-contract.md) | `DELETE /v1/contracts/:contract` | [docs](https://app.ugosign.com/api/docs) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:contact` | [docs](https://app.ugosign.com/api/docs) |
| [Get Contract](actions/get-contract.md) | `GET /v1/contracts/:contract` | [docs](https://app.ugosign.com/api/docs) |
| [Get Contract Custom Vars](actions/get-contract-custom-vars.md) | `GET /v1/contracts/:contract/customVars` | [docs](https://app.ugosign.com/api/docs) |
| [Get Envelope](actions/get-envelope.md) | `GET /v1/envelopes/:envelope` | [docs](https://app.ugosign.com/api/docs) |
| [Get Organization](actions/get-organization.md) | `GET /v1/organization` | [docs](https://app.ugosign.com/api/docs) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://app.ugosign.com/api/docs) |
| [List Contracts](actions/list-contracts.md) | `GET /v1/contracts` | [docs](https://app.ugosign.com/api/docs) |
| [List Envelopes](actions/list-envelopes.md) | `GET /v1/envelopes` | [docs](https://app.ugosign.com/api/docs) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://app.ugosign.com/api/docs) |
| [List Members](actions/list-members.md) | `GET /v1/members` | [docs](https://app.ugosign.com/api/docs) |
| [Search Contracts](actions/search-contracts.md) | `GET /v1/contracts/search` | [docs](https://app.ugosign.com/api/docs) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/:contact` | [docs](https://app.ugosign.com/api/docs) |
| [Update Contract](actions/update-contract.md) | `PATCH /v1/contracts/:contract` | [docs](https://app.ugosign.com/api/docs) |
