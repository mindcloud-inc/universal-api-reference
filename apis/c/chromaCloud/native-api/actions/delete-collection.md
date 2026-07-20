# Delete collection with Chroma Cloud

Deletes a collection from Chroma Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Delete collection](https://docs.trychroma.com/reference/chroma-api/collection/delete-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
