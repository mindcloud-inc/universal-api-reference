# Rebind Report in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/Rebind`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Rebind Report in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/rebind-report-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `reportId` | path | `string` | yes | The report ID to rebind. |
| `datasetId` | body | `string` | yes | The target dataset ID. |
