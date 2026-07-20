# Delete a goal with Asana

Deletes a goal from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `goals/:goal_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a goal](https://developers.asana.com/reference/deletegoal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_gid` | path | `string` | yes | Asana goal gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
