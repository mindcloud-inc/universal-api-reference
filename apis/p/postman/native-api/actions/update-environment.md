# Update Environment with Postman

Updates an existing environment in Postman.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/environments/:environmentId`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Update Environment](https://www.postman.com/postman/postman-public-workspace/request/gwlw6in/update-an-environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | The environment's ID. |
| `patch.op` | body | `string` | yes | — |
| `patch.path` | body | `string` | yes | — |
| `patch.value` | body | `string` | no | — |
