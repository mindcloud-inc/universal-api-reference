# List revisions for a feature with GrowthBook

Retrieves revisions for a GrowthBook feature.

## Endpoint

- **Method:** `GET`
- **Path:** `/features/:id/revisions`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [List revisions for a feature](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `skipPagination` | query | `string` | no | If true, return all matching items and ignore limit/offset. Self-hosted only. Has no effect unless API_ALLOW_SKIP_PAGINATION is set to true or 1. |
| `status` | query | `string` | no | — |
| `author` | query | `string` | no | — |
