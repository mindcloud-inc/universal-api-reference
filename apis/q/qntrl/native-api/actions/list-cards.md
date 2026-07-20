# List Cards with Qntrl

Retrieves a list of cards from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Cards](https://core.qntrl.com/apidoc.html#getAllJobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
