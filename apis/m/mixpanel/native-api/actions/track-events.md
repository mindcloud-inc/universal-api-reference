# Track Events with Mixpanel

Creates new tracked events in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/track`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Track Events](https://developer.mixpanel.com/reference/track-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[].event` | body | `string` | yes | The event name for one tracked event row. |
| `events[].properties.time` | body | `number` | yes | Event time in seconds or milliseconds since UTC epoch. |
| `distinct_id` | body | `string` | yes | Distinct ID for the user who performed the event. |
| `$insert_id` | body | `string` | yes | Unique event identifier used for deduplication. |
| `events[].properties.extraProperties` | body | `object` | no | Additional custom event properties to merge into the event properties object. |
| `verbose` | query | `number` | no | When 1, Mixpanel responds with a JSON object describing success or failure. |
| `ip` | query | `number` | no | When 1, Mixpanel uses the request IP to compute a distinct ID if one is not provided. |
| `img` | query | `number` | no | When 1, Mixpanel returns a 1x1 transparent pixel response. |
| `callback` | query | `string` | no | Optional JavaScript callback name for JSONP-style responses. |
