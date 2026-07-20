# Create Dataset with HoneyHive

Creates a new dataset in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasets`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Dataset](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name. |
| `name` | body | `string` | yes | Dataset name. |
