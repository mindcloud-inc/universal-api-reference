# List Users with Statsig

Retrieves users from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/users`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Users](https://docs.statsig.com/api-reference/users/list-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
| `include_stale_members` | query | `boolean` | no | Whether to include stale company-user membership edges. Defaults to false, which returns only effective current members (matching the Settings UI). |
