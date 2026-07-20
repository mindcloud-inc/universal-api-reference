# Update Application with 100Hires ATS

Updates an existing application in 100Hires ATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/applications/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Update Application](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to update. |
| `stage_id` | body | `number` | no | Optional stage ID to move the application to. |
| `is_disqualified` | body | `boolean` | no | Mark whether the application is disqualified. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |
