# List Group Receiver Events with CleverReach

Retrieves receiver events for a group receiver in CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups.json/:groupId/receivers/:poolId/events`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Group Receiver Events](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Group ID. |
| `pool_id` | path | `string` | yes | ID or email of receiver. |
