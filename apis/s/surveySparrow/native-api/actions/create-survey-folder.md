# Create Survey Folder with SurveySparrow

Creates a new survey folder in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/survey_folders`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Survey Folder](https://developers.surveysparrow.com/rest-apis/post-v-3-survey-folders/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the survey folder |
| `visibility` | body | `list` | yes | Visibility of the survey folder |
| `teams[]` | body | `array<number>` | no | Teams with access |
| `users[]` | body | `array<number>` | no | Users with access |
