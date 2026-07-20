# Delete Patient Tag with Cerbo

Deletes a patient tag from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/patients/:patient_id/tags/:tag_name`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Patient Tag](https://docs.cer.bo/#tag/Patient-Tags/operation/deletePatientTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
| `tag_name` | path | `string` | no |
