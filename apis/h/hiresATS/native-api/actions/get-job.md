# Get Job with 100Hires ATS

Retrieves a job from 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Get Job](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Job ID or alias to retrieve. |
| `include` | query | `string` | no | Optional comma-separated related job resources to include. |
