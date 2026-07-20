# Stop Test with Headless Testing

Stops a running test in Headless Testing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tests/:session_id/stop`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Stop Test](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | Running session identifier from the path. |
