# Get Voice Log with SignalWire

Retrieves a voice log from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/logs/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Get Voice Log](https://signalwire.com/docs/apis/rest/voice-logs/get-voice-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the log. This is the segment_id you can find in Relay call details in your Dashboard UI or in return objects when using the SDK. |
