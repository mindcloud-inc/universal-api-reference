# List Custom Fields with Qntrl

Retrieves custom fields from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/customfield`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Custom Fields](https://core.qntrl.com/apidoc.html#GetAllCustomFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
