# Create Website Domain Research Request with PagePixels

## Endpoint

- **Method:** `POST`
- **Path:** `/api/domain_research_requests`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Create Website Domain Research Request](https://pagepixels.com/app/screenshots-api-documentation#domain-research-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name for this research job. |
| `additional_notes` | body | `string` | no | Optional notes for the research job. |
| `domains[]` | body | `array<string>` | yes | List of domains to analyze. |
| `structures[0].data_type` | body | `string` | yes | The data type to extract for the first structure entry. |
| `structures[0].data_field_name` | body | `string` | yes | The result field name for the first structure entry. |
| `structures[0].data_field_prompt_description` | body | `string` | yes | The extraction prompt for the first structure entry. |
