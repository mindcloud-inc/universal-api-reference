# Delete Vectors with Moorcheh

Deletes vectors from a Moorcheh namespace by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/vectors/delete`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Delete Vectors](https://docs.moorcheh.ai/api-reference/data/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the vector namespace containing vectors to delete. |
| `ids[]` | body | `array<string>` | yes | Array of vector IDs to permanently delete. Moorcheh allows up to 1000 IDs per request. |
