# Import Documents With Upsert with Typesense

Imports documents into Typesense using upsert mode.

## Endpoint

- **Method:** `POST`
- **Path:** `/collections/{{collection}}/documents/import`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Import Documents With Upsert](https://typesense.org/docs/30.0/api/documents.html#action-modes-batch-create-upsert-update-emplace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `documents` | body | `string` | yes | Newline-delimited JSON documents body. |
