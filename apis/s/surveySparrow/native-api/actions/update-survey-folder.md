# Update Survey Folder with SurveySparrow

Updates an existing survey folder in SurveySparrow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/survey_folders/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Update Survey Folder](https://developers.surveysparrow.com/rest-apis/patch-v-3-survey-folders-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the survey folder |
| `name` | body | `string` | no | Name of the survey folder |
| `visibility` | body | `list` | no | Visibility of the survey folder |
| `teams[]` | body | `array<number>` | no | Teams with access |
| `users[]` | body | `array<number>` | no | Users with access |
