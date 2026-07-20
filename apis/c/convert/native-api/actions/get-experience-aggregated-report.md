# Get Experience Aggregated Report with Convert

Retrieves an aggregated report for a Convert experience.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/experiences/:experience_id/aggregated_report`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Experience Aggregated Report](https://api.convert.com/doc/v2/#tag/Experiences-Reports/operation/getExperienceAggregatedReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `experience_id` | path | `string` | yes | Convert experience ID. |
