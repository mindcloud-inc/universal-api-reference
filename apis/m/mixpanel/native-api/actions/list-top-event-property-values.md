# List Top Event Property Values with Mixpanel

Retrieves top event property values from Mixpanel.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/events/properties/values`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [List Top Event Property Values](https://developer.mixpanel.com/reference/query-events-top-property-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `event` | query | `string` | yes | Single event name to inspect. |
| `name` | query | `string` | yes | Event property name to inspect. |
| `limit` | query | `number` | no | Maximum number of values to return. |
