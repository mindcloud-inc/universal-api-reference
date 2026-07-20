# Delete Namespace with Pinecone

Deletes a namespace from a Pinecone index.

## Endpoint

- **Method:** `DELETE`
- **Path:** `{indexHost}/namespaces/:namespace`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Delete Namespace](https://docs.pinecone.io/reference/api/2025-10/data-plane/deletenamespace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace` | path | `string` | yes | The name of the namespace to delete. |
