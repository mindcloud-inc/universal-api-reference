# List Blueprints with Qntrl

Retrieves blueprints from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/blueprint`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Blueprints](https://core.qntrl.com/apidoc.html#GetAllBlueprints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
