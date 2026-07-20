# Get Event with Wooxy

Retrieves an event from your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/custom-event/get`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Event](https://wooxy.com/api-documentation/events/get-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The Wooxy event ID. Use this or Event Name. |
| `name` | body | `string` | no | The Wooxy event name. Use this or Event ID. |
