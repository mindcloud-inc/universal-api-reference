# Create Index with Pinecone

Creates a new index in Pinecone.

## Endpoint

- **Method:** `POST`
- **Path:** `/indexes`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Create Index](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the index to create. |
| `vector_type` | body | `string` | yes | The vector type for the index. |
| `dimension` | body | `number` | yes | The dimension for dense vectors in the index. |
| `metric` | body | `string` | yes | The similarity metric for the index. |
| `spec` | body | `object` | yes | The index specification object, such as a serverless or BYOC deployment spec. |
| `deletion_protection` | body | `string` | no | Whether deletion protection is enabled for the index. |
