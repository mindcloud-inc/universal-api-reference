# Discontinue Patient Supplement with Cerbo

Discontinues an existing patient supplement in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/patients/:pt_id/supplements/:pt_plan_other_id/discontinue`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Discontinue Patient Supplement](https://docs.cer.bo/#tag/Patient-Supplements/operation/discontinuePatientSupplement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | yes | ID of the patient |
| `pt_plan_other_id` | path | `number` | yes | ID of the patient's supplement prescription to discontinue |
| `discontinued_date` | body | `date` | no | Date and time when the supplement was discontinued. If not provided, defaults to the current date/time. |
| `discontinued_note` | body | `string` | no | Reason for discontinuing the supplement |
