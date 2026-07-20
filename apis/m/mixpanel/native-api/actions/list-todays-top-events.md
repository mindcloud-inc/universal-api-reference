# List Today's Top Events with Mixpanel

Retrieves today's top events from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/events/top`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Today's Top Events](https://developer.mixpanel.com/reference/query-top-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `type` | query | `string` | yes | Analysis type: general, unique, or average. |
| `limit` | query | `number` | no | Maximum number of events to return. |
