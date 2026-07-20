# Create Tool with HoneyHive

Creates a new tool in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Tool](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tool name. |
| `type` | body | `string` | yes | Tool type. |
| `task` | body | `string` | yes | Tool task. |
| `parameters` | body | `object` | yes | Tool parameters. |
