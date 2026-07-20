# Get Group Receiver with CleverReach

Retrieves a group receiver from CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups.json/:groupId/receivers/:poolId`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [Get Group Receiver](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | ID of the group. |
| `pool_id` | path | `string` | yes | ID or email of the receiver. |
