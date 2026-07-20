# Get Experience Report Settings with Convert

Retrieves report settings for a Convert experience.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/experiences/:experience_id/report_settings`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Experience Report Settings](https://api.convert.com/doc/v2/#tag/Experiences-Reports/operation/getExperienceReportSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `experience_id` | path | `string` | yes | Convert experience ID. |
