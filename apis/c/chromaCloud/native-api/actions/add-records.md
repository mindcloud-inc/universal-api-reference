# Add records with Chroma Cloud

Adds records to a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/add`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Add records](https://docs.trychroma.com/reference/chroma-api/record/add-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `ids[]` | body | `array<string>` | yes | Unique identifiers for each record. |
| `embeddings[]` | body | `array<array>` | yes | Embedding vectors corresponding to the record IDs. |
| `documents[]` | body | `array<string>` | no | — |
| `metadatas[]` | body | `array<object>` | no | — |
| `uris[]` | body | `array<string>` | no | — |
