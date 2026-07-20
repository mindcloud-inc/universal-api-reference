# Get Patient Supplement with Cerbo

Retrieves patient supplement details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/supplements/:supplement_prescribed_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Supplement](https://docs.cer.bo/#tag/Patient-Supplements/operation/showPatientSupplement)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
| `supplement_prescribed_id` | path | `number` | no |
