# Update Patient Tags with Cerbo

Updates patient tags in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/tags`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Patient Tags](https://docs.cer.bo/#tag/Patient-Tags/operation/updatePatientTags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
| `tags[]` | body | `array<object>` | no |
