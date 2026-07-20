# Vector Search Documents with Typesense

Finds documents in Typesense using vector search.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{{collection}}/documents/search`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Vector Search Documents](https://typesense.org/docs/30.0/api/vector-search.html)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `q` | query | `string` | yes | Text query, often * for vector-only search. |
| `query_by` | query | `string` | yes | Fields to search. |
| `vector_query` | query | `string` | yes | Typesense vector_query parameter. |
