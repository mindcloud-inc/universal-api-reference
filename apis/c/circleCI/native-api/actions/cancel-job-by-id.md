# Cancel Job By ID with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:job_id/cancel`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Cancel Job By ID](https://circleci.com/docs/api/v2/#tag/Job/operation/cancelJobByJobID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | no | Opaque job identifier. |
