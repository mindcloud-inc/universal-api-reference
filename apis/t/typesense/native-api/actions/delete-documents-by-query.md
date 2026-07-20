# Delete Documents By Query with Typesense

Deletes matching documents from a Typesense collection.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/collections/{{collection}}/documents`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Delete Documents By Query](https://typesense.org/docs/30.0/api/documents.html#delete-documents-by-query)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
