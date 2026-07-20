# Copy Survey with SmartSurvey

Copies an existing survey in SmartSurvey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/surveys/{surveyId}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Copy Survey](https://docs.smartsurvey.io/reference/put_surveys-surveyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id that you want to copy |
| `title` | body | `string` | no | The title for the copied survey |
| `nickname` | body | `string` | no | The nickname for the copied survey |
| `open` | body | `boolean` | no | Whether to open the survey as soon as it is copied |
| `account_user_id` | body | `number` | no | The user to assign the survey to |
| `folder_id` | body | `number` | no | The folder id to store the survey in |
