# Groups AssignMyWorkspaceToCapacity with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `AssignToCapacity`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups AssignMyWorkspaceToCapacity](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-assign-my-workspace-to-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | body | `string` | yes | The capacity ID. To unassign from a capacity, use an empty GUID (00000000-0000-0000-0000-000000000000). |
