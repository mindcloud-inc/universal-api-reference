# List Card Comments with Qntrl

Retrieves card comments from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/[:job_id]/comment`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Card Comments](https://core.qntrl.com/apidoc.html#GetAllComments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
