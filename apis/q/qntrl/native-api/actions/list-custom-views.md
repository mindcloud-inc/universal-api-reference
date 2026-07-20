# List Custom Views with Qntrl

Retrieves custom views from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/customview`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Custom Views](https://core.qntrl.com/apidoc.html#GetAllCustomViews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
