# Create Form with QuintaDB

Creates a new form in QuintaDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/entities.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Create Form](https://quintadb.com/api/index#create_form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `name` | body | `string` | yes |
