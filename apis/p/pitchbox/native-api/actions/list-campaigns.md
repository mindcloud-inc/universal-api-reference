# List Campaigns with Pitchbox

## Endpoint

- **Method:** `GET`
- **Path:** `/api/campaigns`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [List Campaigns](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter by campaign id. |
| `name` | query | `string` | no | Filter by campaign name. |
| `q` | query | `string` | no | Filter by response properties. |
| `status` | query | `string` | no | Filter by status: active, archived, or deleted. |
