# Get Case Feedback Data with FuseDesk

Retrieves feedback data for an existing FuseDesk case.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/cases/:caseId/feedback`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Get Case Feedback Data](https://documenter.getpostman.com/view/11014835/SztBc8ix#5d926fba-764f-45b4-aaff-e961cc84efee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | path | `number` | yes | The FuseDesk case ID to inspect feedback for. |
