# Add a Number to a pool with Routee

Adds a number to a pool in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pools/my/:poolId/numbers/:msisdn`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Add a Number to a pool](https://docs.routee.net/reference/add-a-number-to-a-pool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | path | `string` | yes | The number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
| `poolId` | path | `string` | yes | — |
| `poolid` | path | `string` | yes | The tracking id of the pool. |
