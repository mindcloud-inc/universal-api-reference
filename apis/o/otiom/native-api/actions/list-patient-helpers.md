# List Patient Helpers with Otiom

Retrieves helpers for a patient from Otiom.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/patients/:patientid/helpers/`
- **Base URL:** `https://api.otiom.com`
- **Official documentation:** [List Patient Helpers](https://api.otiom.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patientid` | path | `number` | yes | A unique integer value identifying this patient. |
