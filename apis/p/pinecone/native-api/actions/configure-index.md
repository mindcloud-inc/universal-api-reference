# Configure Index with Pinecone

Updates an existing index in Pinecone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/indexes/:index_name`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Configure Index](https://docs.pinecone.io/reference/api/2025-10/control-plane/configure_index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index_name` | path | `string` | yes | The name of the index to configure. |
| `tags` | body | `object` | no | Custom tags to add or update on the index. |
| `deletion_protection` | body | `string` | no | Whether deletion protection is enabled or disabled for the index. |
| `spec` | body | `object` | no | The scaling or deployment specification updates for the index. |
| `embed` | body | `object` | no | The integrated embedding configuration updates for the index. |
