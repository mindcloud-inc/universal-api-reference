# Advance Application To Next Stage with 100Hires ATS

Advances an application to the next stage in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/advance`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Advance Application To Next Stage](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to advance to its next workflow stage. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |
