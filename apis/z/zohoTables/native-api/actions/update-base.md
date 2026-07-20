# Update Base with Zoho Tables

Updates an existing base in Zoho Tables.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bases`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Update Base](https://tables.zoho.com/help/api/v1#BASES-Update-Base)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `portal_id` | query | `number` | yes |
| `base_id` | query | `string` | yes |
| `base_name` | query | `string` | no |
| `base_icon` | query | `number` | no |
| `base_color` | query | `string` | no |
