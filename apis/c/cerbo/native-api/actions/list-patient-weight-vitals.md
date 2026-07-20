# List Patient Weight Vitals with Cerbo

Retrieves patient weight vitals from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/vitals/weight`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Weight Vitals](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientWeightVitals)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
