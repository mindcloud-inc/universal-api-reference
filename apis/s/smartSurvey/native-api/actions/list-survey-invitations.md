# List Survey Invitations with SmartSurvey

Retrieves survey invitations for a SmartSurvey survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/invitations`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [List Survey Invitations](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Invitations you are querying |
| `sent_only` | query | `boolean` | no | A value indicating whether to return only sent invitations |
