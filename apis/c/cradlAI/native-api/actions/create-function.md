# Create Function with Cradl AI

Creates a new function in Cradl AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Create Function](https://docs.cradl.ai/api-reference/post-functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Function name. |
| `description` | body | `string` | no | Function description. |
| `runtime` | body | `list` | no | Runtime used by the function. Accepted values: `nodejs`, `python`. |
| `metadata` | body | `object` | no | Metadata attached to the function. |
