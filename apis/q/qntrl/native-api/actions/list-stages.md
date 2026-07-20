# List Stages with Qntrl

Retrieves a list of stages from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/stage`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Stages](https://core.qntrl.com/apidoc.html#GetAllStages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
