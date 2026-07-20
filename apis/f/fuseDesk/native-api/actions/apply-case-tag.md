# Apply Case Tag with FuseDesk

Applies a tag to an existing FuseDesk case.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/tag/:caseTagId`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Apply Case Tag](https://documenter.getpostman.com/view/11014835/SztBc8ix#5afd2da9-d6c8-41ee-b93b-41b0d5ddd7bc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caseId` | path | `number` | yes |
| `caseTagId` | path | `number` | yes |
