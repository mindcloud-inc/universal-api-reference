# List Report Pages with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/reports/[:reportId]/pages`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Report Pages](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-pages-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `reportId` | path | `string` | yes | The report ID. |
