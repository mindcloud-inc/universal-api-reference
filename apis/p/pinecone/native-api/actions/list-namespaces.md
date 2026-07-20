# List Namespaces with Pinecone

Retrieves namespaces from a Pinecone index.

## Endpoint

- **Method:** `GET`
- **Path:** `{indexHost}/namespaces`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [List Namespaces](https://docs.pinecone.io/reference/api/2025-10/data-plane/listnamespaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prefix` | query | `string` | no | Only return namespaces that start with this prefix. |
