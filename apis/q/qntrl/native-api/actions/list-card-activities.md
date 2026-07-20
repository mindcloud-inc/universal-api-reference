# List Card Activities with Qntrl

Retrieves card activities from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/[:job_id]/activities`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Card Activities](https://core.qntrl.com/apidoc.html#Activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
