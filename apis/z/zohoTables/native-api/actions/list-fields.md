# List Fields with Zoho Tables

Retrieves all fields from Zoho Tables.

## Endpoint

- **Method:** `GET`
- **Path:** `/fields`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [List Fields](https://tables.zoho.com/help/api/v1#FIELDS-List-Fields)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
