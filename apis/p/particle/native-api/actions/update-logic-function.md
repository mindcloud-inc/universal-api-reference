# Update Logic Function with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/logic/functions/:logicFunctionId`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Update Logic Function](https://docs.particle.io/reference/cloud-apis/api/#update-logic-function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logic_function` | body | `object` | yes | Provide a full logic_function object including `name`, `description`, `enabled`, `source`, and `logic_triggers`. |
| `logicFunctionId` | path | `string` | yes | — |
