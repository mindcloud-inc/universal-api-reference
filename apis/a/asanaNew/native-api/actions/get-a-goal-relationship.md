# Get a goal relationship with Asana

Retrieves a goal relationship from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `goal_relationships/:goal_relationship_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a goal relationship](https://developers.asana.com/reference/getgoalrelationship)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_relationship_gid` | path | `string` | yes | Asana goal relationship gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
