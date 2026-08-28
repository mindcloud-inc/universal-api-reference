# Get Universal Action with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/universal/apps/:appSlug/actions/:actionSlug`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Get Universal Action](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionSlug` | path | `string` | yes | Action Slug for this MindCloud v2 request. |
| `appSlug` | path | `string` | yes | App Slug for this MindCloud v2 request. |
| `fields` | query | `string` | no | Optional Fields query parameter documented by the MindCloud v2 API. |
| `version` | query | `string` | no | Optional Version query parameter documented by the MindCloud v2 API. |
