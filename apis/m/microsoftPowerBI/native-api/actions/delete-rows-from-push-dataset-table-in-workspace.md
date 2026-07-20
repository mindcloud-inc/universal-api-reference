# Delete Rows from Push Dataset Table in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/tables/[:tableName]/rows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Rows from Push Dataset Table in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-delete-rows-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `datasetId` | path | `string` | yes | The push dataset ID. |
| `tableName` | path | `string` | yes | The table name whose rows should be deleted. |
