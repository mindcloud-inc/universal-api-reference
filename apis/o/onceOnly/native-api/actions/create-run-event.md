# Create Run Event with OnceOnly

Creates a run event in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Create Run Event](https://docs.onceonly.tech/reference/runs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | body | `string` | yes | Run id that owns the event. |
| `type` | body | `string` | yes | Event type. |
| `ts` | body | `number` | no | Optional event timestamp. |
| `status` | body | `string` | no | Optional event status. |
| `duration_ms` | body | `number` | no | Optional duration in milliseconds. |
| `step` | body | `string` | no | Optional step label. |
| `tool` | body | `string` | no | Optional tool name. |
| `req_id` | body | `string` | no | Optional request id. |
| `lease_id` | body | `string` | no | Optional lease id. |
| `agent_id` | body | `string` | no | Optional agent id. |
| `message` | body | `string` | no | Optional human-readable event message. |
| `data` | body | `object` | no | Optional structured event data object. |
