# Create Logic Function with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/logic/functions`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Create Logic Function](https://docs.particle.io/reference/cloud-apis/api/#create-a-new-logic-function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logic_function` | body | `object` | yes | Provide a full logic_function object including `name`, `description`, `enabled`, `source`, and `logic_triggers`. |
