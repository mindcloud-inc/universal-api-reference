# Update File with Vapi

Updates an existing file in Vapi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/file/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Update File](https://docs.vapi.ai/api-reference/files/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | This is the name of the file. This is just for your own reference. |
