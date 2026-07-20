# Create Patient Custom Vital with Cerbo

Creates a new patient custom vital in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/vitals/:vital_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Custom Vital](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientCustomVital)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `vital_id` | path | `number` | no | — |
| `value` | body | `string` | no | — |
| `abnormal` | body | `boolean` | no | A boolean value to indicate if the reading should be marked as abnormal. If left blank, defaults to false (the vital reading is added as “normal”) |
| `comments` | body | `string` | no | — |
| `date_taken` | body | `string` | no | A string specifying the date and time of the vital reading (if no valid 3-letter timezone specified, defaults to UTC). If left blank, defaults to the current time. |
