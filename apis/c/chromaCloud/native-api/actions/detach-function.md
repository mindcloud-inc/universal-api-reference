# Detach function with Chroma Cloud

Detaches a function from a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/attached_functions/:name/detach`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Detach function](https://docs.trychroma.com/api-reference/function/detach-function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `name` | path | `string` | yes | Attached function name. |
| `delete_output` | body | `boolean` | no | Whether to delete the output collection as well. |
