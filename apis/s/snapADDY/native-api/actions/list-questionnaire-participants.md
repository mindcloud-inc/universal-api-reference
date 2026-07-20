# List Questionnaire Participants with snapADDY

## Endpoint

- **Method:** `GET`
- **Path:** `/visitreport/v1/backend/questionnaires/:questionnaireId/participants/all`
- **Base URL:** `https://api.snapaddy.com`
- **Official documentation:** [List Questionnaire Participants](https://developers.snapaddy.com/visitreport-rest-api/reference/questionnaire-participants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionnaireId` | path | `string` | yes | Questionnaire identifier |
| `limit` | query | `number` | no | Maximum number of participants to return |
| `page` | query | `number` | no | Page number |
| `filter` | query | `string` | no | Filter expression |
