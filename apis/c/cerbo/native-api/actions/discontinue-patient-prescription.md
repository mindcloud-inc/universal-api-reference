# Discontinue Patient Prescription with Cerbo

Discontinues an existing patient prescription in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/patients/:pt_id/rxs/:pt_rx_id/discontinue`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Discontinue Patient Prescription](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/discontinuePatientPrescription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | yes | ID of the patient |
| `pt_rx_id` | path | `number` | yes | ID of the patient's medication prescription to discontinue |
| `discontinued_date` | body | `date` | no | Date and time when the medication was discontinued. If not provided, defaults to the current date/time. |
| `discontinued_reason` | body | `string` | yes | Reason for discontinuing the medication (required) |
