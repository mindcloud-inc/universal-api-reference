# Fork collection with Chroma Cloud

Creates a fork of a collection in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Fork collection](https://docs.trychroma.com/api-reference/collection/fork-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
| `new_name` | body | `string` | yes | — |
