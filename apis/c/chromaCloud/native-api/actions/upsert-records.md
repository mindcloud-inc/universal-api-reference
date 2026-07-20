# Upsert records with Chroma Cloud

Updates records in Chroma Cloud, or creates them if absent.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/upsert`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Upsert records](https://docs.trychroma.com/reference/chroma-api/record/upsert-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `ids[]` | body | `array<string>` | yes | — |
| `embeddings[]` | body | `array<array>` | yes | — |
| `documents[]` | body | `array<string>` | no | — |
| `metadatas[]` | body | `array<object>` | no | — |
| `uris[]` | body | `array<string>` | no | — |
