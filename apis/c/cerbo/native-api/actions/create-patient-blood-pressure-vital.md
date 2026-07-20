# Create Patient Blood Pressure Vital with Cerbo

Creates a new patient blood pressure vital in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/vitals/bp`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Blood Pressure Vital](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientBloodPressureVital)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `systolic` | body | `string` | no | A string specifying the systolic pressure reading |
| `diastolic` | body | `string` | no | A string specifying the diastolic pressure reading |
| `pulse` | body | `string` | no | A string specifying the pulse (b/min) reading |
| `comments` | body | `string` | no | — |
| `date_taken` | body | `string` | no | A string specifying the date and time of the vital reading (if no valid 3-letter timezone specified, defaults to UTC). If left blank, defaults to the current time. |
