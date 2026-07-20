# NextLead: Native API Reference

A consolidated summary of NextLead's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.nextlead.app/en/api-documentation
- **API base URL:** `https://dashboard.nextlead.app`

## Authentication

### API Key

Authenticate with a NextLead automation API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dashboard.nextlead.app/en/api-documentation#identification)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | `POST /api/v2/receive/actions/create-action` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-action-create) |
| [Create Form](actions/create-form.md) | `POST /api/v2/receive/forms/create-form` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-form-create) |
| [Create Sale](actions/create-sale.md) | `POST /api/v2/receive/sales/create-sale` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-sale-create) |
| [Create Structure](actions/create-structure.md) | `POST /api/v2/receive/structure/new-structure` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-structure-create) |
| [Delete Structure](actions/delete-structure.md) | `POST /api/v2/receive/structure/delete-structure` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-structure-delete) |
| [Edit Structure](actions/edit-structure.md) | `POST /api/v2/receive/structure/edit-structure` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-structure-edit) |
| [Find Contact](actions/find-contact.md) | `POST /api/v2/receive/contact/find-contact` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-contact-find) |
| [Get Form](actions/get-form.md) | `GET /api/v2/receive/forms/get-form` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-form-getForm) |
| [Identify Organization](actions/identify-organization.md) | `GET /api/v2/identify-user` | [docs](https://dashboard.nextlead.app/en/api-documentation#identification) |
| [List Action Columns](actions/list-action-columns.md) | `GET /api/v2/receive/actions/get-columns` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-action-getColumns) |
| [List Conversion Statuses](actions/list-conversion-statuses.md) | `GET /api/v2/receive/contact/get-conversion` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-contact-getConversion) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /api/v2/receive/contact/get-custom-fields` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-contact-getCustomFields) |
| [List Lists](actions/list-lists.md) | `GET /api/v2/receive/lists/get-lists` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-list-getLists) |
| [List Sales Columns](actions/list-sales-columns.md) | `GET /api/v2/receive/sales/get-columns` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-sale-getColumns) |
| [List Structures](actions/list-structures.md) | `GET /api/v2/receive/structure/get-structures` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-structure-getStructures) |
| [List Team Members](actions/list-team-members.md) | `GET /api/v2/receive/contact/get-team` | [docs](https://dashboard.nextlead.app/en/api-documentation#receive-contact-getTeam) |
