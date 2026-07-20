# Update Survey with PickFu

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/[:id]`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [Update Survey](https://www.pickfu.com/docs/api-reference/surveys/update-survey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Survey GUID. |
| `name` | body | `string` | no | Survey name. |
| `projectId` | body | `string` | no | Project GUID or numeric ID, or null to remove the project. |
| `questions[]` | body | `array<object>` | no | Questions to replace all existing questions. |
| `tags[]` | body | `array<object>` | no | Tags to replace all existing tags. |
| `targeting[]` | body | `array<string>` | no | Targeting trait permalinks. |
| `reporting[]` | body | `array<string>` | no | Reporting trait permalinks. |
| `country` | body | `string` | no | Two-letter country code. |
| `sample_size` | body | `string` | no | Number of respondents. |
| `survey_intent` | body | `string` | no | Original intent of the survey as interpreted by AI. |
