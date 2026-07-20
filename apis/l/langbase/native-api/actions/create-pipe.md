# Create Pipe with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/pipes`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Create Pipe](https://langbase.com/docs/api-reference/pipe/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique pipe name. |
| `upsert` | body | `boolean` | no | When true, Langbase updates the pipe if the name already exists instead of failing. |
