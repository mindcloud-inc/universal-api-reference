# <img src="https://images.mindcloud.co/apps/icons/zite_1774992036291.png" alt="Zite logo" width="28" height="28"> Zite: Universal API

Manage Zite databases, tables, fields, records, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zite/latest
- **Category:** IT Operations / Database
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zite.com/
- **Vendor API docs:** https://fillout.com/help/database/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Databases](actions/get-databases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in a Zite database. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes an existing table from a Zite database. |
| [Update Table](actions/update-table.md) | PUT | Updates an existing table in a Zite database. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in a Zite table. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from a Zite table. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in a Zite table. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Zite. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes an existing database from Zite. |
| [Get Database by ID](actions/get-database-by-id.md) | GET | Retrieves a specific database from Zite by ID. |
| [Get Databases](actions/get-databases.md) | GET | Retrieves all databases available in Zite. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from a Zite table. |
| [Get Record by ID](actions/get-record-by-id.md) | GET | Retrieves a specific record from Zite by ID. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a specific Zite table. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a Zite table. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a Zite table. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook for a Zite database. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from a Zite database. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions for a Zite database. |

