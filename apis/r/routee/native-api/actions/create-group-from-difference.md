# Create group from difference with Routee

Creates group from difference in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/my/difference`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Create group from difference](https://docs.routee.net/reference/create-group-from-difference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the group to be created. Must be between 2 and 30 characters |
| `groups` | body | `string` | yes | The names of the groups used to create the new group. |
