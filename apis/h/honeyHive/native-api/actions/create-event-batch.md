# Create Event Batch with HoneyHive

Creates a batch of events in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/batch`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Event Batch](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | Events to create. |
