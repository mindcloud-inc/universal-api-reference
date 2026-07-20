# Create a Pool with Routee

Creates a new pool in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/pools/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Create a Pool](https://docs.routee.net/reference/create-a-pool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `poolName` | body | `string` | yes | The name of the pool. |
| `smsSettings` | body | `object` | yes | The SMS settings of the pool |
