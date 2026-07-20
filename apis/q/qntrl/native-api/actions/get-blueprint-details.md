# Get Blueprint Details with Qntrl

Retrieves blueprint details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/blueprint/[:blueprint_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Blueprint Details](https://core.qntrl.com/apidoc.html#ProcessDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_id` | path | `string` | no | Qntrl blueprint ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
