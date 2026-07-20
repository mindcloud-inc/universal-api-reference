# Update Document with Typesense

Updates an existing document in Typesense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collections/{{collection}}/documents/{{id}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Update Document](https://typesense.org/docs/30.0/api/documents.html#update-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `id` | path | `string` | yes | Document ID. |
