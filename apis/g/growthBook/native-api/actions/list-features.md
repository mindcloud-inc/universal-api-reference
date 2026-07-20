# Get all features with GrowthBook

Retrieves features from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/features`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all features](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `projectId` | query | `string` | no | Filter by project id |
| `clientKey` | query | `string` | no | Filter by a SDK connection's client key |
| `skipPagination` | query | `string` | no | If true, return all matching items and ignore limit/offset. Self-hosted only. Has no effect unless API_ALLOW_SKIP_PAGINATION is set to true or 1. |
