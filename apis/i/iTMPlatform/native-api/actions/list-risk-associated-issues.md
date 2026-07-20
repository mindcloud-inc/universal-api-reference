# List Risk Associated Issues with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/project/{ProjectId}/Risk/{RiskId}/AssociatedIssues`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [List Risk Associated Issues](https://developers.itmplatform.com/documentation/#/operations/getAssociatedIssuesOfRisk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `RiskId` | path | `string` | yes | The ITM Platform risk ID. |
