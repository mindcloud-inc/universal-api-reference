# Get Pipe with Langbase

## Endpoint

- **Method:** `GET`
- **Path:** `v1/pipes/:ownerLogin/:pipeName`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Get Pipe](https://langbase.com/docs/api-reference/pipe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownerLogin` | path | `string` | yes | Owner login that owns the pipe. |
| `pipeName` | path | `string` | yes | Pipe name to fetch. |
