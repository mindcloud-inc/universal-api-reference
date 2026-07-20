# Get Document with Typesense

Retrieves a specific document from Typesense.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{{collection}}/documents/{{id}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Get Document](https://typesense.org/docs/30.0/api/documents.html#retrieve-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `id` | path | `string` | yes | Document ID. |
