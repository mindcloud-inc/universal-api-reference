# List Projects with Pitchbox

## Endpoint

- **Method:** `GET`
- **Path:** `/api/projects`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [List Projects](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by project name. |
| `q` | query | `string` | no | Filter by response properties. |
| `id` | query | `number` | no | Filter by project id. |
| `status` | query | `string` | no | Filter by status: active, archived, or deleted. |
