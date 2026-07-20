# Send Survey Invitation Batch with SmartSurvey

Sends a SmartSurvey invitation to multiple recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys/{surveyId}/invitations/{invitationId}/send`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Send Survey Invitation Batch](https://docs.smartsurvey.io/reference/post_surveys-surveyid-invitations-invitationid-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitation you are querying |
| `invitationId` | path | `number` | yes | The invitation id that you are querying |
| `contacts[]` | body | `array<object>` | yes | The list of contacts to send the invitation to |
