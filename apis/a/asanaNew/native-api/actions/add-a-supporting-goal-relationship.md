# Add a supporting goal relationship with Asana

Adds a supporting goal relationship in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/addSupportingRelationship`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a supporting goal relationship](https://developers.asana.com/reference/addsupportingrelationship)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.contribution_weight` | body | `number` | yes | — |
| `data.insert_after` | body | `string` | yes | — |
| `data.insert_before` | body | `string` | yes | — |
| `data.supporting_resource` | body | `string` | yes | — |
| `goal_gid` | path | `string` | yes | Path parameter: goal_gid |
| `opt_fields[]` | query | `array<string>` | no | — |
| `data` | body | `object` | yes | — |
