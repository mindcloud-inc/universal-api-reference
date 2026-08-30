# Create Project with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/projects`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Project](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/projects/guide)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `properties` | body | `object` | yes |
| `properties.hs_name` | body | `string` | yes |
| `properties.hs_pipeline` | body | `string` | yes |
| `properties.hs_pipeline_stage` | body | `string` | yes |
| `properties.hs_description` | body | `string` | no |
| `properties.hs_status` | body | `string` | no |
| `properties.hs_type` | body | `string` | no |
| `properties.hs_target_due_date` | body | `date` | no |
| `properties.hubspot_owner_id` | body | `string` | no |
| `associations[]` | body | `array<object>` | no |
| `associations[].to` | body | `object` | no |
| `associations[].to.id` | body | `string` | no |
| `associations[].types[]` | body | `array<object>` | no |
| `associations[].types[].associationCategory` | body | `string` | no |
| `associations[].types[].associationTypeId` | body | `number` | no |
