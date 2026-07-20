# Get My Work Tasks with OnePlan

Retrieves My Work tasks from OnePlan.

## Endpoint

- **Method:** `GET`
- **Path:** `/mywork/tasks`
- **Base URL:** `https://my.oneplan.ai/api`
- **Official documentation:** [Get My Work Tasks](https://my.oneplan.ai/ApiHelp/Api/GET-api-mywork-tasks_PeriodStart_PeriodEnd_ShowComplete_UserId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PeriodEnd` | query | `string` | no | Optional period end date from the docs. |
| `PeriodStart` | query | `string` | no | Optional period start date from the docs. |
| `ShowComplete` | query | `string` | no | Optional flag to include completed work. |
| `UserId` | query | `string` | no | Optional user identifier filter. |
