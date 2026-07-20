# Disable Case Feedback with FuseDesk

Disables case feedback requests in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/feedback/dontask`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Disable Case Feedback](https://documenter.getpostman.com/view/11014835/SztBc8ix#de345295-df28-4851-a914-ff3d6ec3216b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | path | `number` | yes | The FuseDesk case ID to disable feedback for. |
