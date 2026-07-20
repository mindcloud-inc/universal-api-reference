# Create Index With Integrated Embedding with Pinecone

Creates an index with integrated embedding in Pinecone.

## Endpoint

- **Method:** `POST`
- **Path:** `/indexes/create-for-model`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Create Index With Integrated Embedding](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_for_model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the index to create. |
| `cloud` | body | `string` | yes | The cloud provider where the index is hosted. |
| `region` | body | `string` | yes | The region where the index is created. |
| `embed` | body | `object` | yes | The integrated embedding configuration object, including model, field map, and read/write parameters. |
| `deletion_protection` | body | `string` | no | Whether deletion protection is enabled for the index. |
