# Get Company Hierarchy with DataMerge

Retrieves a company hierarchy from DataMerge by DataMerge ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/hierarchy`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Get Company Hierarchy](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datamerge_id` | query | `string` | yes |
| `include_branches` | query | `boolean` | no |
| `include_names` | query | `boolean` | no |
| `only_subsidiaries` | query | `boolean` | no |
| `max_level` | query | `number` | no |
| `country_code[]` | query | `array<string>` | no |
| `page` | query | `number` | no |
