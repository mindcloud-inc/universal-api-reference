# Patch Workload with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `capacities/[:capacityId]/Workloads/[:workloadName]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch Workload](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/patch-workload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | path | `string` | yes | The capacity ID |
| `workloadName` | path | `string` | yes | The name of the workload |
| `state` | body | `object` | yes | The capacity workload state |
| `maxMemoryPercentageSetByUser` | body | `number` | no | The percentage of the maximum memory that a workload can consume (set by the user) |
