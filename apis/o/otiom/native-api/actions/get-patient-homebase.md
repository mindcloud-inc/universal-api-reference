# Get Patient Homebase with Otiom

Retrieves a patient's homebase from Otiom.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/patients/:patientid/homebase/`
- **Base URL:** `https://api.otiom.com`
- **Official documentation:** [Get Patient Homebase](https://api.otiom.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patientid` | path | `number` | yes | A unique integer value identifying this patient. |
