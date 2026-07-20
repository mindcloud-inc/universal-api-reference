# Get Profitability Report with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/reports/profitability`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Get Profitability Report](https://app.tmetric.com/api-docs/#/Reports/get-accounts-accountId-reports-profitability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `clientId` | query | `number<number>` | no | Optional list of client identifiers. Send multiple values as a string separated by `,`. |
| `endDate` | query | `date` | no | Report end date. |
| `projectId` | query | `number<number>` | no | Optional list of project identifiers. Send multiple values as a string separated by `,`. |
| `projectManagerId` | query | `number<number>` | no | Optional list of project manager identifiers. Send multiple values as a string separated by `,`. |
| `projectStatus` | query | `string` | no | Optional project status filter. |
| `projectType` | query | `string<string>` | no | Optional list of project types. Send multiple values as a string separated by `,`. |
| `startDate` | query | `date` | no | Report start date. |
