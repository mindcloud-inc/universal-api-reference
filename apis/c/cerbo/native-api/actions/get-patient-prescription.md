# Get Patient Prescription with Cerbo

Retrieves patient prescription details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/rxs/:medication_prescribed_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Prescription](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/showPatientPrescription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `medication_prescribed_id` | path | `number` | no | ID of prescribed medication |
