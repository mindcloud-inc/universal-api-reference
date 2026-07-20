# Fetch Records with Criteria with Zoho Tables

Finds records in Zoho Tables by criteria or record IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/fetchRecordsWithCriteria`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Fetch Records with Criteria](https://tables.zoho.com/help/api/v1#RECORDS-Fetch-Record-with-Criteria)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `base_id` | query | `string` | yes |
| `table_id` | query | `string` | yes |
| `view_id` | query | `string` | no |
| `criteria` | query | `string` | no |
| `first_match_only` | query | `boolean` | no |
| `is_case_sensitive` | query | `boolean` | no |
| `is_ids_used_in_params` | query | `boolean` | no |
| `reference_record_id` | query | `string` | no |
| `count` | query | `number` | no |
| `record_ids` | query | `string` | no |
