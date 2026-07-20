# Queue Patient Prescription with Cerbo

Queues a patient prescription request in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/rxs`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Queue Patient Prescription](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/queuePatientPrescription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `enqueue` | query | `boolean` | no | (true by default) If true, the system will insert the drug into the active patient portal queue so that the clinic is notified and can review the proposed addition. This replicates the functionality of the patient portal queue. |
| `drug_id` | body | `number` | yes | An integer identifier for a drug as returned from a /v1/drugs/search/:term query. |
| `notes` | body | `string` | no | — |
