# Search Bases with Zoho Tables

Finds bases in Zoho Tables by search string.

## Endpoint

- **Method:** `GET`
- **Path:** `/searchBases`
- **Base URL:** `https://tables.zoho.com/api/v1`
- **Official documentation:** [Search Bases](https://tables.zoho.com/help/api/v1#BASES-Search-Bases)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `search_string` | query | `string` | yes |
| `portal_id` | query | `number` | yes |
| `workspace_id` | query | `string` | no |
