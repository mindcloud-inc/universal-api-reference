# List Top Event Properties with Mixpanel

Retrieves top event properties from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/events/properties/top`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Top Event Properties](https://developer.mixpanel.com/reference/query-events-top-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `event` | query | `string` | yes | Single event name to inspect. |
| `limit` | query | `number` | no | Maximum number of properties to return. |
