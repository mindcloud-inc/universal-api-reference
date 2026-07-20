# Refill Patient Prescription with Cerbo

Queues a patient prescription refill in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/rxs/refill`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Refill Patient Prescription](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/refillPatientPrescription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `original_prescription_id` | body | `number` | yes | An integer identifier for an existing prescription for this patient as returned from a /v1/patients/:patient_id/rxs GET query. |
| `notes` | body | `string` | no | — |
| `agreed_to_terms` | body | `string` | no | A string value representing agreement to terms. If not set, defaults to "No terms agreed to". |
