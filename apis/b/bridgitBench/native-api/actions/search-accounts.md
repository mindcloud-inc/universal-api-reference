# Search Accounts with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/Accounts/_filter`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Search Accounts](https://developers.gobridgit.com/reference/accounts_queryfilter)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `predicates` | body | `object` | no | — |
| `predicates.accountIds[]` | body | `array<number>` | yes | — |
| `predicates.state` | body | `list<string>` | yes | Accepted values: `Active`, `All`, `Deactivated`. |
| `predicates.name` | body | `string` | no | — |
| `predicates.organizationId` | body | `string` | no | — |
| `predicates.isDemo` | body | `boolean` | no | — |
| `sort` | body | `object` | no | — |
| `sort.sortBy` | body | `list<number>` | yes | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `sort.direction` | body | `list<string>` | yes | Accepted values: `Asc`, `Desc`. |
