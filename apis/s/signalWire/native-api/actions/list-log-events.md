# List Log Events with SignalWire

Retrieves voice log events from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/logs/{id}/events`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Log Events](https://signalwire.com/docs/apis/rest/voice-logs/list-voice-log-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the log. This is the segment_id you can find in Relay call details in your Dashboard UI or in return objects when using the SDK. |
