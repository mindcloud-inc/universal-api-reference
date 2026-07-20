# Get collection by ID with Chroma Cloud

Retrieves a collection by ID from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/by-id/:collection_id`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get collection by ID](https://docs.trychroma.com/reference/chroma-api/collection/get-collection-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
