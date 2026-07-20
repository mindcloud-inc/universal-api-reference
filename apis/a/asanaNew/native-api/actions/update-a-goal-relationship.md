# Update a goal relationship with Asana

Updates a goal relationship in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `goal_relationships/:goal_relationship_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a goal relationship](https://developers.asana.com/reference/updategoalrelationship)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_relationship_gid` | path | `string` | yes | Path parameter: goal_relationship_gid |
| `opt_fields[]` | query | `array<string>` | no | — |
| `data` | body | `object` | yes | — |
