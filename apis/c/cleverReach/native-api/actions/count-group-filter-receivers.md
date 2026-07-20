# Count Group Filter Receivers with CleverReach

Retrieves a receiver count for a group filter in CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/groups.json/:groupId/filters/:filterId/count`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [Count Group Filter Receivers](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_id` | path | `string` | yes | Group ID. |
| `group_id` | path | `string` | no | Filter ID. |
