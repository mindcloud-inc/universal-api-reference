# Attach function with Chroma Cloud

Attaches a function to a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/functions/attach`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Attach function](https://docs.trychroma.com/api-reference/function/attach-function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `name` | body | `string` | yes | — |
| `function_id` | body | `string` | yes | — |
| `output_collection` | body | `string` | yes | — |
| `params` | body | `object` | no | — |
