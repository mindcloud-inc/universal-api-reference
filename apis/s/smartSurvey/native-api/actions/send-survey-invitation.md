# Send Survey Invitation with SmartSurvey

Sends a SmartSurvey invitation to one recipient.

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys/{surveyId}/invitations/{invitationId}/sendone`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Send Survey Invitation](https://docs.smartsurvey.io/reference/post_surveys-surveyid-invitations-invitationid-sendone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitation you are querying |
| `invitationId` | path | `number` | yes | The invitation id that you are querying |
| `name` | body | `string` | yes | The name of the contact to send the invitation to |
| `email` | body | `string` | no | The email address of the target for this invitation (if an email invitation) |
| `mobile` | body | `string` | no | The mobile/cell number for the target for this invitation (if an SMS invitation) |
| `custom_columns[]` | body | `array<object>` | no | Custom column values for this recipient, if needed |
