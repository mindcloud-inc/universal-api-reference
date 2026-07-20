# Create Field with Zoho Tables

Creates a new field in Zoho Tables.

## Endpoint

- **Method:** `POST`
- **Path:** `/fields`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Create Field](https://tables.zoho.com/help/api/v1#FIELDS-Create-Field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `type` | query | `number` | no |
