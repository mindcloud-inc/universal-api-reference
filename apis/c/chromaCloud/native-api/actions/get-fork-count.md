# Get fork count with Chroma Cloud

Retrieves a collection fork count from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/fork_count`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get fork count](https://docs.trychroma.com/reference/chroma-api/collection/get-fork-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
