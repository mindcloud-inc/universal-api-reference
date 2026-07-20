# List Issue Risks with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Projects/{ProjectId}/Issues/{IssueId}/Risks`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [List Issue Risks](https://developers.itmplatform.com/documentation/#/operations/getAssociatedProjectRiskV2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `IssueId` | path | `string` | yes | The ITM Platform issue ID. |
