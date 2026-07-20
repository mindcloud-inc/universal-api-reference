# List Tasks with MoreApp

Retrieves tasks from MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/{{formId}}/tasks/filter/{{page}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Tasks](https://docs.moreapp.com/docs/developer-docs/e1305a3576723-list-all-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `formId` | path | `string` | yes | MoreApp form identifier. |
| `page` | path | `number` | yes | Task result page number. |
| `pageSize` | body | `number` | no | Optional number of tasks to return per page. |
