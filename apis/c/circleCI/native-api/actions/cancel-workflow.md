# Cancel Workflow with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/:id/cancel`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Cancel Workflow](https://circleci.com/docs/api/v2/#tag/Workflow/operation/cancelWorkflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Opaque workflow identifier. |
