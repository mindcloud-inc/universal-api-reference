# List feature revisions with GrowthBook

Retrieves feature revisions from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/revisions`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [List feature revisions](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `skipPagination` | query | `string` | no | If true, return all matching items and ignore limit/offset. Self-hosted only. Has no effect unless API_ALLOW_SKIP_PAGINATION is set to true or 1. |
| `featureId` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `author` | query | `string` | no | — |
| `mine` | query | `string` | no | If true, return only revisions authored by or contributed to by the calling user. Requires a user-scoped API key. Mutually exclusive with `author`. |
