# Create Namespace with Pinecone

Creates a namespace in a Pinecone index.

## Endpoint

- **Method:** `POST`
- **Path:** `{indexHost}/namespaces`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Create Namespace](https://docs.pinecone.io/reference/api/2025-10/data-plane/createnamespace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the namespace. |
