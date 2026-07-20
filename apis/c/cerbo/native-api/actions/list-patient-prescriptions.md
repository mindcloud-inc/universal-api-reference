# List Patient Prescriptions with Cerbo

Retrieves patient prescriptions from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/rxs`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Prescriptions](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/listPatientPrescriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
