# List Survey Invitation Responses with SmartSurvey

Retrieves responses for a SmartSurvey invitation.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/invitations/{invitationId}/list`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [List Survey Invitation Responses](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid-list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitation you are querying |
| `invitationId` | path | `number` | yes | The invitation id whose responses you are querying |
| `status` | query | `number` | no | Filter responses by status. Possible values: 0=All, 1=Sent, 2=Queued, 3=Completed, 4=Pending, 5=Failed, 6=Opened, 7=Viewed, 8=OptedOut, 9=Deleted |
