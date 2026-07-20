# Create Project Function with Rentman

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/projectfunctions`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [Create Project Function](https://api.rentman.net/#operation/createProjectFunction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric ID of the parent project. |
| `subproject` | body | `string` | yes | Subproject reference, for example /subprojects/0. |
| `cost_rate` | body | `string` | yes | Cost rate reference, for example /rates/0. |
| `price_rate` | body | `string` | yes | Price rate reference, for example /rates/0. |
| `name` | body | `string` | no | Function name on packing lists. |
| `type` | body | `string` | no | Function type. |
| `amount` | body | `number` | no | Function amount. |
