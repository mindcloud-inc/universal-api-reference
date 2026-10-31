# List Saved Filters with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/my-filters`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Saved Filters](https://developers.gobridgit.com/reference/userfilters_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `type` | query | `list<string>` | no | The filter type to return in the result Accepted values: `People`, `Project`, `Roles`. |
| `name` | query | `string` | no | The filter name by partial match to return in the result |
