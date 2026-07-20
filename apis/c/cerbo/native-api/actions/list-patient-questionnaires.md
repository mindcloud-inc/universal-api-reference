# List Patient Questionnaires with Cerbo

Retrieves patient questionnaires from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/questionnaires`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Questionnaires](https://docs.cer.bo/#tag/Questionnaires/operation/listPatientQuestionnaires)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `extended_details` | query | `boolean` | no | Defaults to false, but can be overridden. If false (good for looping through lots of questionnaires) it will not return the actual key-value responses that the patient submitted and instead return a NULL value for the raw_data property. |
