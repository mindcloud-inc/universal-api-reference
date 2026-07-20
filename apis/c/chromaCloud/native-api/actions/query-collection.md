# Query collection with Chroma Cloud

Queries a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/query`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Query collection](https://docs.trychroma.com/reference/chroma-api/record/query-collection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `query_embeddings[]` | body | `array<array>` | yes | Query embedding vectors. |
| `n_results` | body | `number` | no | — |
| `include[]` | body | `array<string>` | no | — |
| `where` | body | `object` | no | — |
