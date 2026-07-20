# Create Patient Questionnaire with Cerbo

Creates a new patient questionnaire in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/questionnaires`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Questionnaire](https://docs.cer.bo/#tag/Questionnaires/operation/createPatientQuestionnaire)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `questionnaire_type` | body | `string` | no | — |
| `questionnaire_name` | body | `string` | no | — |
| `html_content` | body | `string` | yes | An HTML-formatted string that will serve as the human-readable version of the patient responses |
| `raw_data` | body | `object` | yes | An object with key-value pairs that will represent the structured data underlying the patient responses. This allows us to analyze their response-data. |
