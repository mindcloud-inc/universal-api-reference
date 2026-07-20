# Get Custom View Details with Qntrl

Retrieves custom view details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/customview/[:customview_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Custom View Details](https://core.qntrl.com/apidoc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customview_id` | path | `string` | no | Qntrl custom view ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
