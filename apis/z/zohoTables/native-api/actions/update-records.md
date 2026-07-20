# Update Records with Zoho Tables

Updates records in Zoho Tables by criteria or record IDs.

## Endpoint

- **Method:** `PUT`
- **Path:** `/records`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Update Records](https://tables.zoho.com/help/api/v1#RECORDS-Update-Record-with-Criteria)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
| `data` | query | `string` | yes |
| `is_ids_used_in_data` | query | `boolean` | no |
| `criteria` | query | `string` | no |
| `is_ids_used_in_params` | query | `boolean` | no |
| `first_match_only` | query | `boolean` | no |
| `is_case_sensitive` | query | `boolean` | no |
| `is_upsert_needed` | query | `boolean` | no |
| `record_ids` | query | `string` | no |
