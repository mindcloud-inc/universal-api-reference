# List PDF Jobs with TemplateFox

Retrieves PDF jobs from TemplateFox.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/pdf/jobs`
- **Base URL:** `https://api.templatefox.com`
- **Official documentation:** [List PDF Jobs](https://templatefox.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of jobs to return. |
| `offset` | query | `number` | no | Number of jobs to skip. |
| `status` | query | `string` | no | Optional job status filter. |
