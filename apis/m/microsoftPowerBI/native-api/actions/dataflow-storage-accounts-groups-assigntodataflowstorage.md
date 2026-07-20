# Groups AssignToDataflowStorage with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/AssignToDataflowStorage`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups AssignToDataflowStorage](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflow-storage-accounts/groups-assign-to-dataflow-storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowStorageId` | body | `string` | yes | The Power BI dataflow storage account ID. To unassign the specified workspace from a Power BI dataflow storage account, use an empty GUID (00000000-0000-0000-0000-000000000000). |
