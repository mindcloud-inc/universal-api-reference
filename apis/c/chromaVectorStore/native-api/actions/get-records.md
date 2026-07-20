# Get Records with Chroma Vector Store

Retrieves collection records from Chroma by ID or metadata filter.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/get`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get Records](https://docs.trychroma.com/reference/chroma-api/record/get-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | — |
| `database` | path | `string` | yes | — |
| `ids[]` | body | `array<string>` | no | Optional IDs to fetch |
| `include[]` | body | `array<string>` | no | Optional record fields to include |
| `tenant` | path | `string` | yes | — |
