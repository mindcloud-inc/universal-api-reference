# Mark Application As Hired with 100Hires ATS

Marks an application as hired in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/hire`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Mark Application As Hired](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to mark as hired. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |
