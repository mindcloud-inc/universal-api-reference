# Get Project Report with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/reports/projects`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Get Project Report](https://app.tmetric.com/api-docs/#/Reports/get-accounts-accountId-reports-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `clientId` | query | `number<number>` | no | Optional list of client identifiers. Send multiple values as a string separated by `,`. |
| `endDate` | query | `date` | no | Report end date. |
| `includeDone` | query | `boolean` | no | Include done projects in the report. |
| `projectId` | query | `number<number>` | no | Optional list of project identifiers. Send multiple values as a string separated by `,`. |
| `startDate` | query | `date` | no | Report start date. |
| `teamId` | query | `number<number>` | no | Optional list of team identifiers. Send multiple values as a string separated by `,`. |
| `userId` | query | `number<number>` | no | Optional list of user identifiers. Send multiple values as a string separated by `,`. |
