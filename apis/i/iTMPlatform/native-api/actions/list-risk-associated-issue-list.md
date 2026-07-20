# List Risk Associated Issue List with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/project/{ProjectId}/Risk/{RiskId}/AssociatedIssueList`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [List Risk Associated Issue List](https://developers.itmplatform.com/documentation/#/operations/getAssociatedProjectIssueList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `RiskId` | path | `string` | yes | The ITM Platform risk ID. |
