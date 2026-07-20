# Get PDF Job with TemplateFox

Retrieves a PDF job from TemplateFox.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/pdf/jobs/{{job_id}}`
- **Base URL:** `https://api.templatefox.com`
- **Official documentation:** [Get PDF Job](https://templatefox.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Async PDF job ID. |
