# Create Patient Weight Vital with Cerbo

Creates a new patient weight vital in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/vitals/weight`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Weight Vital](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientWeightVital)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `weight` | body | `string` | no | A string specifying the weight reading |
| `units` | body | `string` | no | A string specifying the unit (“lbs” or “kg”) |
| `comments` | body | `string` | no | — |
| `date_taken` | body | `string` | no | A string specifying the date and time of the vital reading (if no valid 3-letter timezone specified, defaults to UTC). If left blank, defaults to the current time. |
