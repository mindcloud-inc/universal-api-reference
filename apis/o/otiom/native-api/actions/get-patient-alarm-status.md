# Get Patient Alarm Status with Otiom

Retrieves a patient's alarm status from Otiom.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/patients/:id/has_alarm/`
- **Base URL:** `https://api.otiom.com`
- **Official documentation:** [Get Patient Alarm Status](https://api.otiom.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | A unique integer value identifying this patient. |
