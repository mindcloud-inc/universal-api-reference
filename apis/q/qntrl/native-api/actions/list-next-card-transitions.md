# List Next Card Transitions with Qntrl

Retrieves next card transitions from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/nexttransitions/[:job_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Next Card Transitions](https://core.qntrl.com/apidoc.html#GetNextTransitions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
