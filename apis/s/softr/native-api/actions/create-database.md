# Create Database with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `/databases`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Create Database](https://docs.softr.io/softr-api/softr-database-api/databases/create-a-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | The ID of the workspace where the database will be created. |
| `name` | body | `string` | yes | The database name. |
| `description` | body | `string` | no | The database description. |
