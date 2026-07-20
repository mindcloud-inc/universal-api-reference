# Get collection with Chroma Cloud

Retrieves a collection from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get collection](https://docs.trychroma.com/reference/chroma-api/collection/get-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
