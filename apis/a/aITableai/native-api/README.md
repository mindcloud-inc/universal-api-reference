# AITable.ai: Native API Reference

A consolidated summary of AITable.ai's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.aitable.ai/api/reference/
- **API base URL:** `https://aitable.ai`

## Authentication

### API Token

Authenticate with an AITable API token sent as a bearer token.

### Credentials

- **API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.aitable.ai/api/quick-start/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `pageNum` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Datasheet](actions/create-datasheet.md) | `POST /fusion/v1/spaces/:spaceId/datasheets` | [docs](https://developers.aitable.ai/api/reference/#create-datasheet) |
| [Create Embedded Link](actions/create-embedded-link.md) | `POST /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks` | [docs](https://developers.aitable.ai/api/reference/#create-embedded-links) |
| [Create Field](actions/create-field.md) | `POST /fusion/v1/spaces/:spaceId/datasheets/:datasheetId/fields` | [docs](https://developers.aitable.ai/api/reference/#create-field) |
| [Create Records](actions/create-records.md) | `POST /fusion/v1/datasheets/:datasheetId/records` | [docs](https://developers.aitable.ai/api/reference/#create-records) |
| [Create Team](actions/create-team.md) | `POST /fusion/v1/spaces/:spaceId/teams` | [docs](https://developers.aitable.ai/api/reference/#create-a-team) |
| [Delete Embedded Link](actions/delete-embedded-link.md) | `DELETE /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks/:linkId` | [docs](https://developers.aitable.ai/api/reference/#delete-embedded-link) |
| [Delete Field](actions/delete-field.md) | `DELETE /fusion/v1/spaces/:spaceId/datasheets/:datasheetId/fields/:fieldId` | [docs](https://developers.aitable.ai/api/reference/#delete-field) |
| [Delete Records](actions/delete-records.md) | `DELETE /fusion/v1/datasheets/:datasheetId/records` | [docs](https://developers.aitable.ai/api/reference/#delete-record) |
| [Get Member](actions/get-member.md) | `GET /fusion/v1/spaces/:spaceId/members/:unitId` | [docs](https://developers.aitable.ai/api/reference/#get-a-member) |
| [Get Node](actions/get-node.md) | `GET /fusion/v1/spaces/:spaceId/nodes/:nodeId` | [docs](https://developers.aitable.ai/api/reference/#get-node-details) |
| [List Embedded Links](actions/list-embedded-links.md) | `GET /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks` | [docs](https://developers.aitable.ai/api/reference/#get-list-of-embedded-links) |
| [List Fields](actions/list-fields.md) | `GET /fusion/v1/datasheets/:datasheetId/fields` | [docs](https://developers.aitable.ai/api/reference/#get-field) |
| [List Nodes](actions/list-nodes.md) | `GET /fusion/v1/spaces/:spaceId/nodes` | [docs](https://developers.aitable.ai/api/reference/#get-node-list) |
| [List Records](actions/list-records.md) | `GET /fusion/v1/datasheets/:datasheetId/records` | [docs](https://developers.aitable.ai/api/reference/#get-records) |
| [List Role Units](actions/list-role-units.md) | `GET /fusion/v1/spaces/:spaceId/roles/:unitId/units` | [docs](https://developers.aitable.ai/api/reference/#list-units-under-the-role) |
| [List Roles](actions/list-roles.md) | `GET /fusion/v1/spaces/:spaceId/roles` | [docs](https://developers.aitable.ai/api/reference/#list-roles) |
| [List Spaces](actions/list-spaces.md) | `GET /fusion/v1/spaces` | [docs](https://developers.aitable.ai/api/reference/#get-the-list-of-spaces) |
| [List Sub Teams](actions/list-sub-teams.md) | `GET /fusion/v1/spaces/:spaceId/teams/:unitId/children` | [docs](https://developers.aitable.ai/api/reference/#list-sub-teams) |
| [List Team Members](actions/list-team-members.md) | `GET /fusion/v1/spaces/:spaceId/teams/:unitId/members` | [docs](https://developers.aitable.ai/api/reference/#list-the-team-members) |
| [List Views](actions/list-views.md) | `GET /fusion/v1/datasheets/:datasheetId/views` | [docs](https://developers.aitable.ai/api/reference/#get-view) |
| [Update Records](actions/update-records.md) | `PATCH /fusion/v1/datasheets/:datasheetId/records` | [docs](https://developers.aitable.ai/api/reference/#update-records) |
| [Update Team](actions/update-team.md) | `PUT /fusion/v1/spaces/:spaceId/teams/:unitId` | [docs](https://developers.aitable.ai/api/reference/#update-a-team) |
