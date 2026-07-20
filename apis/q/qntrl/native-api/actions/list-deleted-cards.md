# List Deleted Cards with Qntrl

Retrieves deleted cards from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/job/deletedjobs`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Deleted Cards](https://core.qntrl.com/apidoc.html#getDeletedJobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deleted_time` | query | `string` | no | Fetch cards deleted after this epoch-milliseconds timestamp. |
| `layout_id` | query | `string` | no | Qntrl layout ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
