# Create Database with QuintaDB

Creates a new database in QuintaDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Create Database](https://quintadb.com/api/index#create_database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_name` | body | `string` | yes | Name for the new QuintaDB database. |
| `form_name` | body | `string` | yes | Default form name created with the new QuintaDB database. |
