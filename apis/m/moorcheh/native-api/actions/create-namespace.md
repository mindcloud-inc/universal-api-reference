# Create Namespace with Moorcheh

Creates a new namespace in Moorcheh.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Create Namespace](https://docs.moorcheh.ai/api-reference/namespaces/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | body | `string` | yes | Unique namespace name using only alphanumeric characters, hyphens, and underscores. |
| `type` | body | `string` | yes | Namespace type: text for documents or vector for pre-computed embeddings. |
| `vector_dimension` | body | `number` | no | Required for vector namespaces. Dimension of vectors to be stored, such as 1536. |
