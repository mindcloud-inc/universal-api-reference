# Duplicate Base with Zoho Tables

Creates a duplicate base in Zoho Tables.

## Endpoint

- **Method:** `POST`
- **Path:** `/bases`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Duplicate Base](https://tables.zoho.com/help/api/v1#BASES-Duplicate-Base)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `portal_id` | query | `number` | yes |
| `workspace_id` | query | `string` | yes |
| `base_id` | query | `string` | yes |
| `base_name` | query | `string` | no |
| `base_icon` | query | `number` | no |
| `base_color` | query | `string` | no |
| `is_data_needed` | query | `boolean` | no |
