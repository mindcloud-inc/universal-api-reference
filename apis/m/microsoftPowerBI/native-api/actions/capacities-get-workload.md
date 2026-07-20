# Get Workload with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `capacities/[:capacityId]/Workloads/[:workloadName]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Workload](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-workload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | path | `string` | yes | The capacity ID |
| `workloadName` | path | `string` | yes | The name of the workload |
