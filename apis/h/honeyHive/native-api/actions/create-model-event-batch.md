# Create Model Event Batch with HoneyHive

Creates a batch of model events in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/model/batch`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Model Event Batch](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_events[]` | body | `array<object>` | yes | Model events to create. |
