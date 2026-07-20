# Oneflow: Native API Reference

A consolidated summary of Oneflow's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.oneflow.com/reference
- **API base URL:** `https://api.oneflow.com/v1`

## Authentication

### API Token + User Email

Connect Oneflow with a custom auth payload containing an API token and user email.

### Credentials

- **API Token:** `apiKey` · required · The Oneflow API token generated from the Oneflow Marketplace.
- **User Email:** `userEmail` · required · The Oneflow user email used for request authorization checks.

Send these headers with each API request:

```http
x-oneflow-api-token: <apiKey>
x-oneflow-user-email: <userEmail>
```

[Official authentication documentation](https://developer.oneflow.com/docs/authentication-and-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Access Link](actions/create-access-link.md) | `POST /contracts/:contractId/participants/:participantId/access_link` | [docs](https://developer.oneflow.com/reference/create-an-access-link) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.oneflow.com/reference/create-a-contact) |
| [Create Contract](actions/create-contract.md) | `POST /contracts/create` | [docs](https://developer.oneflow.com/reference/create-a-contract) |
| [Create Participant](actions/create-participant.md) | `POST /contracts/:contractId/parties/:partyId/participants` | [docs](https://developer.oneflow.com/reference/create-a-participant) |
| [Create Party](actions/create-party.md) | `POST /contracts/:contractId/parties` | [docs](https://developer.oneflow.com/reference/create-a-party) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developer.oneflow.com/reference/get-a-contact-by-id) |
| [Get Contract](actions/get-contract.md) | `GET /contracts/:id` | [docs](https://developer.oneflow.com/reference/get-a-contract-by-id) |
| [Get Contract Create Data](actions/get-contract-create-data.md) | `GET /helpers/contract_create_data` | [docs](https://developer.oneflow.com/reference/get-data-to-create-a-contract) |
| [Get Contract File](actions/get-contract-file.md) | `GET /contracts/:contractId/files/:fileId` | [docs](https://developer.oneflow.com/reference/get-a-contract-file-by-id) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://developer.oneflow.com/reference/get-a-template-by-id) |
| [Get Template Type](actions/get-template-type.md) | `GET /template_types/:id` | [docs](https://developer.oneflow.com/reference/get-template-type-by-id) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.oneflow.com/reference/get-contacts-in-a-workspace) |
| [List Contract Data Fields](actions/list-contract-data-fields.md) | `GET /contracts/:contractId/data_fields` | [docs](https://developer.oneflow.com/reference/get-contract-data-fields) |
| [List Contract Files](actions/list-contract-files.md) | `GET /contracts/:contractId/files` | [docs](https://developer.oneflow.com/reference/get-contract-files) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://developer.oneflow.com/reference/get-contracts) |
| [List Parties](actions/list-parties.md) | `GET /contracts/:contractId/parties` | [docs](https://developer.oneflow.com/reference/get-parties) |
| [List Template Types](actions/list-template-types.md) | `GET /template_types` | [docs](https://developer.oneflow.com/reference/get-template-types) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developer.oneflow.com/reference/get-templates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.oneflow.com/reference/get-users-in-an-account) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://developer.oneflow.com/reference/get-workspaces) |
| [Publish Contract](actions/publish-contract.md) | `POST /contracts/:id/publish` | [docs](https://developer.oneflow.com/reference/publish-a-contract-by-id) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developer.oneflow.com/reference/update-a-contact-by-id) |
| [Update Contract](actions/update-contract.md) | `PUT /contracts/:id` | [docs](https://developer.oneflow.com/reference/update-a-contract-by-id) |
| [Update Contract Data Field Value](actions/update-contract-data-field-value.md) | `PUT /contracts/:contractId/data_fields/:dataFieldId` | [docs](https://developer.oneflow.com/reference/update-a-contract-data-field-value) |
