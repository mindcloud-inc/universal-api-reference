# Create Record with Zoho Tables

Creates a new record in Zoho Tables.

## Endpoint

- **Method:** `POST`
- **Path:** `/records`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Create Record](https://tables.zoho.com/help/api/v1#RECORDS-Create-Record-with-Data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
| `field_ids_with_values` | query | `string` | no |
| `field_ids` | query | `string` | no |
| `values` | query | `string` | no |
