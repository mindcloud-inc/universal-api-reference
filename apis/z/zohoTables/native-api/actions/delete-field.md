# Delete Field with Zoho Tables

Deletes an existing field from Zoho Tables.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fields`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Delete Field](https://tables.zoho.com/help/api/v1#FIELDS-Delete-Field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `field_id` | query | `string` | yes |
