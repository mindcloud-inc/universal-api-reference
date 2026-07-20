# Duplicate Table with Zoho Tables

Creates a duplicate table in Zoho Tables.

## Endpoint

- **Method:** `POST`
- **Path:** `/tables`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Duplicate Table](https://tables.zoho.com/help/api/v1#TABLES-Duplicate-Table)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `table_name` | query | `string` | no |
| `is_duplicate_with_records` | query | `boolean` | no |
