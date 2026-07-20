# Get Group with Splitwise

Retrieves a group's details from Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_group/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Get Group](https://dev.splitwise.com/#tag/groups/paths/~1get_group~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise group ID to retrieve. |
