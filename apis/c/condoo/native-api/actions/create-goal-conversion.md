# Create Goal Conversion with condoo

Creates a new goal conversion in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/goals-conversions`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Create Goal Conversion](https://trk.condoo.systems/en/api-documentation/goals-conversions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | body | `number` | no | Optional event ID. |
| `goal_id` | body | `number` | yes | Required goal ID. |
| `session_id` | body | `number` | no | Optional session ID. |
| `visitor_id` | body | `number` | no | Optional visitor ID. |
