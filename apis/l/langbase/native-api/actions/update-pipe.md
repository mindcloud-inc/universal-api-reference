# Update Pipe with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/pipes/:pipeName`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Update Pipe](https://langbase.com/docs/api-reference/pipe/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeName` | path | `string` | yes | Pipe name to update. |
| `description` | body | `string` | no | Updated pipe description. |
