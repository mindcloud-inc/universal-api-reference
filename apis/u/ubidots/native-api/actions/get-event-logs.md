# Get Event Logs with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:event_key/logs/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Event Logs](https://docs.ubidots.com/reference/get-event-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_key` | path | `string` | yes | The event ID or key. |
