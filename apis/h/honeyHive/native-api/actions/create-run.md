# Create Run with HoneyHive

Creates a new evaluation run in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/runs`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Run](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name. |
| `name` | body | `string` | yes | Run name. |
| `event_ids[]` | body | `array<string>` | yes | Event IDs for the run. |
