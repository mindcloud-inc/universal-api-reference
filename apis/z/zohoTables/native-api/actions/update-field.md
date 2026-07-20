# Update Field with Zoho Tables

Updates an existing field in Zoho Tables.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fields`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Update Field](https://tables.zoho.com/help/api/v1#FIELDS-Update-Field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `field_id` | query | `string` | yes |
| `field_name` | query | `string` | no |
| `type` | query | `number` | yes |
