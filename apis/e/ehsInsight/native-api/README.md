# EHS Insight: Native API Reference

A consolidated summary of EHS Insight's API configuration and 11 documented operations.

- **API base URL:** `https://{companyName}.ehsinsight.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Company Name:** `companyName` · optional

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Entity](actions/add-entity.md) | `POST /v4/entity/:entityName/add` |  |
| [Create User Contact](actions/create-user-contact.md) | `POST /v6/entity/UserContact/add` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [Get Entity Items](actions/get-entity-items.md) | `GET /v4/entity/:entityName/list?:customparams` |  |
| [Get Hierarchy List](actions/get-hierarchy-list.md) | `GET /v4/hierarchy/list` |  |
| [Get Single Item](actions/get-single-item.md) | `GET /v4/entity/:entityName/fetch/:rowuid` |  |
| [List Entities](actions/list-entities.md) | `GET /v6/entity/list?:customparams` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [List Roles](actions/list-roles.md) | `GET /v6/role/list?:customparams` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [List User Contacts](actions/list-user-contacts.md) | `GET /v6/entity/UserContact/list?:customparams` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [Get Entity Schema](actions/new-action1.md) | `GET /v4/entity/:entityName/schema` |  |
| [Update Entity](actions/update-entity.md) | `POST /v4/entity/:entityName/update` |  |
| [Update User Contact](actions/update-user-contact.md) | `POST /v6/entity/UserContact/update` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
