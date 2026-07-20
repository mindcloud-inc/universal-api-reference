# Update records with Chroma Cloud

Updates records in a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/update`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Update records](https://docs.trychroma.com/reference/chroma-api/record/update-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `ids[]` | body | `array<string>` | yes | — |
| `documents[]` | body | `array<string>` | no | — |
| `embeddings[]` | body | `array<array>` | no | — |
| `metadatas[]` | body | `array<object>` | no | — |
| `uris[]` | body | `array<string>` | no | — |
