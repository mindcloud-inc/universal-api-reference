# Delete Document with Typesense

Deletes a specific document from Typesense.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/collections/{{collection}}/documents/{{id}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Delete Document](https://typesense.org/docs/30.0/api/documents.html#delete-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `id` | path | `string` | yes | Document ID. |
