# Get Survey Invitation with SmartSurvey

Retrieves a survey invitation from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/invitations/{invitationId}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Invitation](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitation you are querying |
| `invitationId` | path | `number` | yes | The invitation id that you are querying |
