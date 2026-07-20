# Update Function with Cradl AI

Updates an existing function in Cradl AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/functions/:functionId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Update Function](https://docs.cradl.ai/api-reference/patch-functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Identifier of the function to update. |
| `name` | body | `string` | no | Updated function name. |
| `description` | body | `string` | no | Updated function description. |
| `metadata` | body | `object` | no | Updated metadata attached to the function. |
