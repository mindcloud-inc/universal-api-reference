# Create Table with NocoDB

Creates a new table in NocoDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/meta/bases/:baseId/tables`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Create Table](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `title` | body | `string` | yes | Title of the table. |
| `description` | body | `string` | no | Description of the table. |
| `source_id` | body | `string` | no | Data source identifier for sourced tables. |
