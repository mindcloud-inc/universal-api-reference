# Get indexing status with Chroma Cloud

Retrieves collection indexing status from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases/:database/collections/:collection_id/indexing_status`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get indexing status](https://docs.trychroma.com/reference/chroma-api/record/get-indexing-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Collection UUID. |
