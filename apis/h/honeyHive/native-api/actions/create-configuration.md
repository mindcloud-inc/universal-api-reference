# Create Configuration with HoneyHive

Creates a new configuration in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/configurations`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Configuration](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name. |
| `name` | body | `string` | yes | Configuration name. |
| `provider` | body | `string` | yes | Configuration provider. |
| `parameters` | body | `object` | yes | Configuration parameters. |
