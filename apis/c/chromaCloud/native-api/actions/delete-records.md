# Delete records with Chroma Cloud

Deletes records from a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/delete`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Delete records](https://docs.trychroma.com/reference/chroma-api/record/delete-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `ids[]` | body | `array<string>` | no | — |
| `where` | body | `object` | no | Metadata filter used to select records. |
