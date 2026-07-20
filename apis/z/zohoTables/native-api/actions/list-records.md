# List Records with Zoho Tables

Retrieves table records from Zoho Tables.

## Endpoint

- **Method:** `GET`
- **Path:** `/records`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [List Records](https://tables.zoho.com/help/api/v1#DATA-List-Data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
| `record_id` | query | `string` | no |
| `count` | query | `number` | no |
