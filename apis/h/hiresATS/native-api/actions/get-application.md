# Get Application with 100Hires ATS

Retrieves an application from 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Get Application](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to retrieve. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |
