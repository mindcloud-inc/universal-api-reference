# Get attached function with Chroma Cloud

Retrieves an attached function from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/functions/:function_name`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get attached function](https://docs.trychroma.com/api-reference/function/get-attached-function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `function_name` | path | `string` | yes | — |
