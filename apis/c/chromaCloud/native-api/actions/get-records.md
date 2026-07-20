# Get records with Chroma Cloud

Retrieves records from a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/get`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get records](https://docs.trychroma.com/reference/chroma-api/record/get-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `ids[]` | body | `array<string>` | no | — |
| `where` | body | `object` | no | — |
| `include[]` | body | `array<string>` | no | Fields to include in the response. |
