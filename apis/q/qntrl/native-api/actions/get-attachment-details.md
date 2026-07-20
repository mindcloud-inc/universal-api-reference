# Get Attachment Details with Qntrl

Retrieves attachment details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/[:job_id]/attachment/[:attachment_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Attachment Details](https://core.qntrl.com/apidoc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `string` | no | Qntrl attachment ID. |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
