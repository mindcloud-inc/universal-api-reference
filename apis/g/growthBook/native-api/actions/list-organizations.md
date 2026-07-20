# Get all organizations (only for super admins on multi-org Enterprise Plan only) with GrowthBook

Retrieves organizations from your GrowthBook account.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all organizations (only for super admins on multi-org Enterprise Plan only)](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search string to search organization names, owner emails, and external ids by |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
