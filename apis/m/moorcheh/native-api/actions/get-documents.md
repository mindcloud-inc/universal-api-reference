# Get Documents with Moorcheh

Retrieves specific documents from a Moorcheh namespace by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/documents/get`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Get Documents](https://docs.moorcheh.ai/api-reference/data/get-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the namespace containing the documents. |
| `ids[]` | body | `array<string>` | yes | Array of document IDs to retrieve. Moorcheh allows up to 100 IDs per request. |
