# Resume Discovery Task with Extruct AI

Resumes a discovery task in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/discovery_tasks/:task_id/resume`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Resume Discovery Task](https://docs.extruct.ai/api-reference/discover/resume-company-discovery-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Deep Search task identifier. |
| `desired_new_results` | body | `number` | no | Additional result count to request. |
