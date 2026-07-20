# Get Survey Invitation Fields with SmartSurvey

Retrieves custom fields for a SmartSurvey invitation.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/invitations/{invitationId}/fields`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Invitation Fields](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitation you are querying |
| `invitationId` | path | `number` | yes | The invitation whose fields you are querying |
