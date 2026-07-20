# Delete Documents with Moorcheh

Deletes documents from a Moorcheh namespace by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/documents/delete`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Delete Documents](https://docs.moorcheh.ai/api-reference/data/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the text namespace containing documents to delete. |
| `ids[]` | body | `array<string>` | yes | Array of document IDs to permanently delete. Moorcheh allows up to 1000 IDs per request. |
