# Get Card Details with Qntrl

Retrieves card details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/[:job_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Card Details](https://core.qntrl.com/apidoc.html#GetJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
