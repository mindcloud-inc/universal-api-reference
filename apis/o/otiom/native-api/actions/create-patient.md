# Create Patient with Otiom

Creates a new patient in Otiom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/patients/`
- **Base URL:** `https://api.otiom.com`
- **Official documentation:** [Create Patient](https://api.otiom.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Patient first name. |
| `last_name` | body | `string` | no | Patient last name. |
| `level` | body | `number` | no | Safety level for the patient. |
| `low_battery_power_save_mode` | body | `boolean` | no | Whether Otiom should enter power save mode below 30% battery. |
