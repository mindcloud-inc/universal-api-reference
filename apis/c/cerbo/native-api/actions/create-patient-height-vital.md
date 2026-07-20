# Create Patient Height Vital with Cerbo

Creates a new patient height vital in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/vitals/height`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Height Vital](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientHeightVital)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `height` | body | `string` | no | A string specifying the height reading |
| `units` | body | `string` | no | A string specifying the unit (inches or “cm”) |
| `comments` | body | `string` | no | — |
| `date_taken` | body | `string` | no | A string specifying the date and time of the vital reading (if no valid 3-letter timezone specified, defaults to UTC). If left blank, defaults to the current time. |
