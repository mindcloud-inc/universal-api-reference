# Complete Task with MoreApp

Completes a task in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}/complete`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Complete Task](https://docs.moreapp.com/docs/developer-docs/56175a9cab2d8-complete-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
