# Update Database with QuintaDB

Updates an existing database in QuintaDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/:app_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update Database](https://quintadb.com/api/index#update_database)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `name` | body | `string` | yes |
