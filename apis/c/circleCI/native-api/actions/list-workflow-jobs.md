# List Workflow Jobs with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow/:id/job`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Workflow Jobs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/listWorkflowJobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Opaque workflow identifier. |
| `page-token` | query | `string` | no | Pagination cursor returned by CircleCI. |
