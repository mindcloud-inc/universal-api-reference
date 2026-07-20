# Edit a Pool with Routee

Updates an existing pool in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pools/my/:poolId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Edit a Pool](https://docs.routee.net/reference/edit-a-pool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `poolId` | path | `string` | yes | The tracking id of the pool. |
| `poolName` | body | `string` | no | The name of the pool. |
| `smsSettings` | body | `object` | no | The SMS settings of the pool. |
