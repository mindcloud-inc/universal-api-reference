# Get Annotation Reply Job Status with Dify

Retrieves annotation reply job status from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/annotation-reply/:action/status/:job_id`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Get Annotation Reply Job Status](https://docs.dify.ai/api-reference/annotations/get-annotation-reply-job-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Annotation reply action. |
| `job_id` | path | `string` | yes | Annotation reply job ID. |
