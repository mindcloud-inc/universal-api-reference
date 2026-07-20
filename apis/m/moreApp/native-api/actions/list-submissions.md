# List Submissions with MoreApp

Retrieves submissions from MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/filter/{{page}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Submissions](https://docs.moreapp.com/docs/developer-docs/9a6201b9c0c73-list-all-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `formId` | path | `string` | yes | MoreApp form identifier. |
| `page` | path | `number` | yes | Submission page number. |
| `pageSize` | body | `number` | no | Optional number of submissions to return per page. |
