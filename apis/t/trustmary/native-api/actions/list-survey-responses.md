# List Survey Responses with Trustmary

Retrieves responses for a survey from Trustmary.

## Endpoint

- **Method:** `GET`
- **Path:** `/survey/:surveyId/responses`
- **Base URL:** `https://api.trustmary.io/v1`
- **Official documentation:** [List Survey Responses](https://help.trustmary.com/api#/paths/~1survey~1{survey_id}~1responses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Trustmary survey ID. |
