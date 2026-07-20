# Upsert Document with Typesense

Creates or updates a document in Typesense.

## Endpoint

- **Method:** `POST`
- **Path:** `/collections/{{collection}}/documents`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Upsert Document](https://typesense.org/docs/30.0/api/documents.html#upsert-a-single-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `document` | body | `object` | yes | Document JSON body. |
