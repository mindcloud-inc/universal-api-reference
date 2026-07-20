# Remove Case Tag with FuseDesk

Removes a tag from an existing FuseDesk case.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/untag/:caseTagId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Remove Case Tag](https://documenter.getpostman.com/view/11014835/SztBc8ix#f906c62f-77b0-4d26-bd9e-5047d7db8395)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caseId` | path | `number` | yes |
| `caseTagId` | path | `number` | yes |
