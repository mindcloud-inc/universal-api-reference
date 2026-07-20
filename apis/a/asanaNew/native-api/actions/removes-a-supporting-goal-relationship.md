# Removes a supporting goal relationship with Asana

Removes a supporting goal relationship in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/removeSupportingRelationship`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Removes a supporting goal relationship](https://developers.asana.com/reference/removesupportingrelationship)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.supporting_resource` | body | `string` | yes | — |
| `goal_gid` | path | `string` | yes | Asana goal gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `data.supporting_resource` | body | `string` | yes | Asana supporting resource parameter. |
