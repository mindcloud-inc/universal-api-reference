# Import Events with Mixpanel

Creates new events in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/import`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Import Events](https://developer.mixpanel.com/reference/import-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[].event` | body | `string` | yes | The event name for one imported event row. |
| `events[].properties.time` | body | `number` | yes | Event time in seconds or milliseconds since UTC epoch. |
| `distinct_id` | body | `string` | yes | Distinct ID for the user who performed the event. |
| `$insert_id` | body | `string` | yes | Unique event identifier used for deduplication. |
| `events[].properties.extraProperties` | body | `object` | no | Additional custom event properties to merge into the event properties object. |
| `strict` | query | `number` | no | When 1, Mixpanel validates the batch and returns detailed errors for failed records. |
| `project_id` | query | `number` | no | Required if using service account authentication for this request. |
