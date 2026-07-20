# Generate Related Job Positions with SharpAPI

Creates related job positions in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/related_job_positions`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Related Job Positions](https://sharpapi.com/en/catalog/ai/hr-tech/related-job-positions-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Job position to generate related roles for. |
| `language` | body | `string` | no | Language for the related job positions output. |
| `max_quantity` | body | `number` | no | Maximum number of related job positions to generate. |
