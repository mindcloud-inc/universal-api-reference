# Fork Collection with Chroma Vector Store

Creates a fork of an existing collection in Chroma.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Fork Collection](https://docs.trychroma.com/api-reference/collection/fork-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID |
| `database` | path | `string` | yes | Database name |
| `new_name` | body | `string` | yes | Name for the forked collection |
| `tenant` | path | `string` | yes | Tenant UUID |
