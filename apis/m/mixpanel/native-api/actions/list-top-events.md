# List Top Events with Mixpanel

Retrieves top events from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/events/names`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Top Events](https://developer.mixpanel.com/reference/query-months-top-event-names)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `type` | query | `string` | yes | Analysis type: general, unique, or average. |
| `limit` | query | `number` | no | Maximum number of event names to return. |
