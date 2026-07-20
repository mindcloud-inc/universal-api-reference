# Search records with Chroma Cloud

Searches records in a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/search`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Search records](https://docs.trychroma.com/reference/chroma-api/record/search-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `searches[]` | body | `array<object>` | yes | Array of Search API search payloads. |
| `read_level` | body | `string` | no | Read level for consistency vs performance. |
