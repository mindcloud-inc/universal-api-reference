# List Universal Actions with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/universal/apps/:appSlug/actions`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List Universal Actions](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appSlug` | path | `string` | yes | App Slug for this MindCloud v2 request. |
| `fields` | query | `string` | no | Optional Fields query parameter documented by the MindCloud v2 API. |
| `includeArguments` | query | `string` | no | Optional Include Arguments query parameter documented by the MindCloud v2 API. |
| `limit` | query | `number` | no | Optional Limit query parameter documented by the MindCloud v2 API. |
| `offset` | query | `number` | no | Optional Offset query parameter documented by the MindCloud v2 API. |
| `q` | query | `string` | no | Optional Search Query query parameter documented by the MindCloud v2 API. |
| `verbosity` | query | `string` | no | Optional Verbosity query parameter documented by the MindCloud v2 API. |
| `version` | query | `string` | no | Optional Version query parameter documented by the MindCloud v2 API. |
