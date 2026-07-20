# Update Tool with HoneyHive

Updates an existing tool in HoneyHive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tools`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Update Tool](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Tool ID. |
| `name` | body | `string` | yes | Tool name. |
| `parameters` | body | `object` | yes | Tool parameters. |
