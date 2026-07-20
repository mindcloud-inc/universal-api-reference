# Inistate: Native API Reference

A consolidated summary of Inistate's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0
- **OpenAPI specification:** https://api.swaggerhub.com/apis/Inistate/InistateAPI/1.0.0/swagger.json
- **API base URL:** `https://api.inistate.com`

## Authentication

### API Key

Use your Inistate API key from Account > Integration.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · Inistate workspace ID required for the authenticated module-discovery scope and shared request header mapping.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://community.inistate.com/t/api-key-location-instructions/62)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Stage0 Entry](actions/create-stage0-entry.md) | `POST /api/activity` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Delete Stage0 Entry](actions/delete-stage0-entry.md) | `POST /api/activity` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Duplicate Stage0 Entry](actions/duplicate-stage0-entry.md) | `POST /api/activity` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Stage0 Create Form](actions/get-stage0-create-form.md) | `POST /api/activity/form` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Stage0 Edit Form](actions/get-stage0-edit-form.md) | `POST /api/activity/form` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Stage0 Listing Metadata](actions/get-stage0-listing-metadata.md) | `POST /api/workspace/list` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Stage0 Quick View Form](actions/get-stage0-quick-view-form.md) | `POST /api/activity/form` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Stage0 View Form](actions/get-stage0-view-form.md) | `POST /api/activity/form` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/workspace/:workspaceIdParam` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [List Stage0 Entries](actions/list-stage0-entries.md) | `POST /api/workspace/list` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/workspace` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Run Stage0 Activity](actions/run-stage0-activity.md) | `POST /api/activity` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
| [Update Stage0 Entry](actions/update-stage0-entry.md) | `POST /api/activity` | [docs](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0) |
