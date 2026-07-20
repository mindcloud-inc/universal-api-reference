# Delete Case Tag with FuseDesk

Archives an existing case tag in FuseDesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/casetags/:caseTagId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Delete Case Tag](https://documenter.getpostman.com/view/11014835/SztBc8ix#c1ae161d-bdad-40bc-9ac8-e1d28bd9f931)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseTagId` | path | `number` | yes | The FuseDesk case tag ID to delete. |
