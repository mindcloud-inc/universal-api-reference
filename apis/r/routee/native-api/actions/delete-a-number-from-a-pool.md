# Delete a number from a pool with Routee

Removes a number from a pool in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pools/my/:poolId/numbers/:msisdn`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Delete a number from a pool](https://docs.routee.net/reference/delete-a-number-from-a-pool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `poolid` | path | `string` | yes | The tracking id of the pool. |
| `poolId` | path | `string` | yes | — |
| `msisdn` | path | `string` | yes | The number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
