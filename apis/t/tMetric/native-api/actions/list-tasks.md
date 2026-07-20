# List Tasks with TMetric

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/tasks`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [List Tasks](https://app.tmetric.com/api-docs/#/Tasks/get-accounts-accountId-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `AfterDate` | query | `date` | no | Return tasks due on or after this date. |
| `Assignee` | query | `number` | no | User identifier where 0 is unassigned. |
| `AssigneeGroup` | query | `number` | no | Team identifier. |
| `BeforeDate` | query | `date` | no | Return tasks due on or before this date. |
| `ClientList` | query | `number<number>` | no | List of client identifiers. Send multiple values as a string separated by `,`. |
| `Completed` | query | `boolean` | no | Filter by completion status. |
| `Creator` | query | `number` | no | User identifier who created the task. |
| `ProjectList` | query | `number<number>` | no | List of project identifiers. Send multiple values as a string separated by `,`. |
| `Source` | query | `string` | no | Task source filter. |
| `TagList` | query | `number<number>` | no | List of tag identifiers. Send multiple values as a string separated by `,`. |
