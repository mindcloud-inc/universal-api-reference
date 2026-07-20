# Update Configuration with HoneyHive

Updates an existing configuration in HoneyHive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/configurations/{id}`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Update Configuration](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Configuration ID. |
| `project` | body | `string` | yes | Project name. |
| `name` | body | `string` | yes | Configuration name. |
| `provider` | body | `string` | yes | Configuration provider. |
| `parameters` | body | `object` | yes | Configuration parameters. |
