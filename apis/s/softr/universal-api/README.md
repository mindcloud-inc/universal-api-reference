# <img src="https://images.mindcloud.co/apps/icons/softr-logo-1_1773065706642.png" alt="Softr logo" width="28" height="28"> Softr: Universal API

Build portals, internal tools, dashboards, and business apps without code.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/softr/latest
- **Category:** IT Operations / Database
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.softr.io
- **Vendor API docs:** https://docs.softr.io/softr-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Databases](actions/list-databases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Authentication Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Authentication Token](actions/validate-authentication-token.md) | GET |  |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST |  |
| [Delete Database](actions/delete-database.md) | DELETE |  |
| [Get Database](actions/get-database.md) | GET |  |
| [List Databases](actions/list-databases.md) | GET |  |
| [Update Database](actions/update-database.md) | PUT |  |

### Magic Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate User Magic Link](actions/generate-user-magic-link.md) | POST |  |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST |  |
| [Delete Record](actions/delete-record.md) | DELETE |  |
| [Get Record](actions/get-record.md) | GET |  |
| [List Records](actions/list-records.md) | GET |  |
| [Search Records](actions/search-records.md) | GET |  |
| [Update Record](actions/update-record.md) | PUT |  |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST |  |
| [Delete Table](actions/delete-table.md) | DELETE |  |
| [Get Table](actions/get-table.md) | GET |  |
| [List Tables](actions/list-tables.md) | GET |  |
| [Update Table](actions/update-table.md) | PUT |  |

### Table Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Table Field](actions/add-table-field.md) | POST |  |
| [Delete Table Field](actions/delete-table-field.md) | DELETE |  |
| [Get Table Field](actions/get-table-field.md) | GET |  |
| [Update Table Field](actions/update-table-field.md) | PUT |  |

### Table View

| Action | Method | Description |
| --- | --- | --- |
| [List Table Views](actions/list-table-views.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Sync Users](actions/sync-users.md) | PUT |  |

