# Get number of records with Chroma Cloud

Retrieves a collection record count from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/count`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get number of records](https://docs.trychroma.com/reference/chroma-api/record/get-number-of-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
