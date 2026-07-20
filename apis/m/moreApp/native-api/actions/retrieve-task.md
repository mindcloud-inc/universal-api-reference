# Retrieve Task with MoreApp

Retrieves a task from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Task](https://docs.moreapp.com/docs/developer-docs/a2c30297eb5a8-retrieve-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
