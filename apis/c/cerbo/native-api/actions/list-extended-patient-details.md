# List Extended Patient Details with Cerbo

Retrieves extended patient details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:id/extended_details`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Extended Patient Details](https://docs.cer.bo/#tag/Extended-Patient-Details/operation/getExtendedPatientDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The ID of the patient. |
| `anonymize` | query | `boolean` | no | The return values will strip PHI identifiers from the chart including: names, street-level addresses, telephone numbers (area codes will remain), date-of-birth (year of birth will remain) and some questionnaire answers. Because ever client has different questionnaires, you will want to make sure you further anonymize the results if your questionnaires include requests for identifying information |
