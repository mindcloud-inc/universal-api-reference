# Get Report Folder Details with Qntrl

Retrieves report folder details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/reportfolder/[:reportfolder_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Report Folder Details](https://core.qntrl.com/apidoc.html#GetFolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `reportfolder_id` | path | `string` | no | Qntrl report folder ID. |
