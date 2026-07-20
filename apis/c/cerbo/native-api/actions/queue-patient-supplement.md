# Queue Patient Supplement with Cerbo

Queues a patient supplement request in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/supplements`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Queue Patient Supplement](https://docs.cer.bo/#tag/Patient-Supplements/operation/queuePatientSupplement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `enqueue` | query | `boolean` | no | (true by default) If true, the system will insert the supplement into the active patient portal queue so that the clinic is notified and can review the proposed addition. This replicates the functionality of the patient portal queue. |
| `supplement_id` | body | `number` | yes | An integer identifier for a supplement as returned from a /v1/supplements/search/:term query. |
| `notes` | body | `string` | no | — |
