# Groups AssignToCapacity with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/AssignToCapacity`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups AssignToCapacity](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-assign-to-capacity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `capacityId` | body | `string` | yes | The capacity ID. To unassign from a capacity, use an empty GUID (00000000-0000-0000-0000-000000000000). |
