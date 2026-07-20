# Stacker: Native API Reference

A consolidated summary of Stacker's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview
- **API base URL:** `https://api.go.stackerhq.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Integration-Key: <apiKey>
```

[Official authentication documentation](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/authentication)

### Integration Key

Connect Stacker with your personal Integration Key

### Credentials

- **Integration Key:** `apiKey` · required · Your personal Stacker Integration Key

Send these headers with each API request:

```http
X-Integration-Key: <apiKey>
```

[Official authentication documentation](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create and Update Records](actions/bulk-create-and-update-records.md) | `POST /api/external/objects/:object_sid/bulk-records/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
| [Create Record](actions/create-record.md) | `POST /api/external/objects/:object_sid/records/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
| [Delete Record](actions/delete-record.md) | `DELETE /api/external/objects/:object_sid/records/:record_sid/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
| [Get Record](actions/get-record.md) | `GET /api/external/objects/:object_sid/records/:record_sid/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
| [List Accounts](actions/list-accounts.md) | `GET /api/external/accounts/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields) |
| [List Action Buttons](actions/list-action-buttons.md) | `GET /api/external/objects/:object_sid/action-buttons/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields) |
| [List Fields](actions/list-fields.md) | `GET /api/external/objects/:object_sid/fields/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields) |
| [List Objects](actions/list-objects.md) | `GET /api/external/objects/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields) |
| [List Stacks](actions/list-stacks.md) | `GET /api/external/stacks/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields) |
| [Search Records](actions/search-records.md) | `POST /api/external/objects/:object_sid/search/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
| [Update Record](actions/update-record.md) | `PATCH /api/external/objects/:object_sid/records/:record_sid/` | [docs](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions) |
