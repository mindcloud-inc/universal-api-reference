# Delete Record with Zoho Tables

Deletes a record from Zoho Tables.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/records`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Delete Record](https://tables.zoho.com/help/api/v1#RECORDS-Delete-Record)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
| `record_id` | query | `string` | yes |
