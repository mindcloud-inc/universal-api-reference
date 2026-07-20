# Request Case Feedback Now with FuseDesk

Requests case feedback immediately in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/feedback/request`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Request Case Feedback Now](https://documenter.getpostman.com/view/11014835/SztBc8ix#796c2bc2-1efc-48d3-abfa-be6ead9045c5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | path | `number` | yes | The FuseDesk case ID to request feedback for immediately. |
