# Update Survey Result Sharing with SmartSurvey

Updates result sharing settings for a SmartSurvey survey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/resultsharing`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Update Survey Result Sharing](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-resultsharing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose results sharing you want to configure |
| `action` | body | `boolean` | yes | Whether to enable results sharing or not |
| `code` | body | `string` | no | The sharing code. If blank, a random code will be generated |
| `permissions` | body | `string` | no | The permissions information in the format e.g. 1-0-1-1... |
| `password` | body | `string` | no | A password for the results (optional but recommended) |
