# List Active Blueprints with Qntrl

Retrieves active blueprints from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/blueprint/active`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Active Blueprints](https://core.qntrl.com/apidoc.html#getActiveBlueprints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
