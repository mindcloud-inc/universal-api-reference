# Create Base with Zoho Tables

Creates a new base in Zoho Tables.

## Endpoint

- **Method:** `POST`
- **Path:** `/bases`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Create Base](https://tables.zoho.com/help/api/v1#BASES-Create-Base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | query | `number` | yes | Portal ID |
| `workspace_id` | query | `string` | yes | Workspace ID |
| `base_name` | query | `string` | no | Base name |
