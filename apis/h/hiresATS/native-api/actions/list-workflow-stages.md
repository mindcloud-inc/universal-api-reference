# List Workflow Stages with 100Hires ATS

Lists the workflow stages in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/stages`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List Workflow Stages](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `number` | no | Optional target company ID. Defaults to the authenticated company. |
| `workflow_id` | query | `number` | no | Optional workflow ID to restrict stages to a specific workflow. |
| `job_id` | query | `number` | no | Optional job ID to load the workflow stages used by a specific job. |
