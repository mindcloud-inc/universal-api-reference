# Create or Update Folder with Rulebricks

Creates or updates a rule folder in Rulebricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/folders`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Create or Update Folder](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description of the folder |
| `name` | body | `string` | yes | Name of the folder |
