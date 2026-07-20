# List Card Attachments with Qntrl

Retrieves card attachments from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/[:job_id]/attachment`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Card Attachments](https://core.qntrl.com/apidoc.html#GetAttachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Qntrl card ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
