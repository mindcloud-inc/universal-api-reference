# Update collection with Chroma Cloud

Updates a collection in Chroma Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Update collection](https://docs.trychroma.com/reference/chroma-api/collection/update-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `new_name` | body | `string` | no | — |
| `new_metadata` | body | `object` | no | — |
