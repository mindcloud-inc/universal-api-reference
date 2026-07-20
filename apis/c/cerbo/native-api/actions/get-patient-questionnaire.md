# Get Patient Questionnaire with Cerbo

Retrieves patient questionnaire details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/questionnaires/:questionnaire_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Questionnaire](https://docs.cer.bo/#tag/Questionnaires/operation/showPatientQuestionnaire)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
| `questionnaire_id` | path | `number` | no |
| `extended_details` | query | `boolean` | no |
