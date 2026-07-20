# Enable Case Feedback with FuseDesk

Enables case feedback requests in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/feedback/doask`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Enable Case Feedback](https://documenter.getpostman.com/view/11014835/SztBc8ix#b55af1e9-0f7d-475d-bc38-0c72a6adc0b5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | path | `number` | yes | The FuseDesk case ID to enable feedback for. |
