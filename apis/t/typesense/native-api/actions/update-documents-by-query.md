# Update Documents By Query with Typesense

Updates matching documents in a Typesense collection.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collections/{{collection}}/documents`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Update Documents By Query](https://typesense.org/docs/30.0/api/documents.html#update-documents-by-query)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
