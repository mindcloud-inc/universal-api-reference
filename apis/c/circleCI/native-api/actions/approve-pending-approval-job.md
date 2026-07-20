# Approve Pending Approval Job with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/:id/approve/:approval_request_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Approve Pending Approval Job](https://circleci.com/docs/api/v2/#tag/Workflow/operation/approvePendingApprovalJobById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approval_request_id` | path | `string` | no | Approval request identifier. |
| `id` | path | `string` | no | Opaque workflow identifier. |
