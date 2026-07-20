# Rerun Workflow with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/:id/rerun`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Rerun Workflow](https://circleci.com/docs/api/v2/#tag/Workflow/operation/rerunWorkflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enable_ssh` | body | `string` | no | Enable SSH for rerun jobs. |
| `from_failed` | body | `string` | no | Rerun only failed jobs when true. |
| `id` | path | `string` | no | Opaque workflow identifier. |
| `jobs` | body | `string` | no | Subset of jobs to rerun. |
| `sparse_tree` | body | `string` | no | Rerun only selected jobs when true. |
