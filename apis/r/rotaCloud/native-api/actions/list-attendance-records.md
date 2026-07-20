# List Attendance Records with RotaCloud

Lists attendance records in RotaCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/attendance`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Attendance Records](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | Unix timestamp for the start of the attendance window. |
| `end` | query | `number` | yes | Unix timestamp for the end of the attendance window. |
