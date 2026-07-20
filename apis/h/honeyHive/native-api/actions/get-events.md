# Get Events with HoneyHive

Finds events in HoneyHive by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/export`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Get Events](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name associated with the event. |
| `filters[]` | body | `array<object>` | yes | Event filters. |
