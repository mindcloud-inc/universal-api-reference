# Clone Report with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/Clone`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Clone Report](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/clone-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `name` | body | `string` | yes | The new report name |
| `targetModelId` | body | `string` | no | Optional. Parameter for specifying the target associated dataset ID. If not provided, the new report will be associated with the same dataset as the source report. |
| `targetWorkspaceId` | body | `string` | no | Optional. Parameter for specifying the target workspace ID. An empty GUID (00000000-0000-0000-0000-000000000000) indicates **My workspace**. If this parameter isn't provided, the new report will be cloned within the same workspace as the source report. |
