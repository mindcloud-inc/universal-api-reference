# Search Contacts with DataMerge

Starts a DataMerge contact search by company and filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/search`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Search Contacts](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | no |
| `company_list` | body | `string` | no |
| `max_results_per_company` | body | `number` | yes |
| `location` | body | `object` | no |
| `job_titles` | body | `object` | no |
| `persona_id` | body | `string` | no |
| `list` | body | `string` | no |
| `enrich_fields[]` | body | `array<string>` | yes |
| `webhook` | body | `string` | no |
