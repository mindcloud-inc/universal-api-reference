# Create Attendance Record with RotaCloud

Creates an attendance record in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/attendance`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Attendance Record](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `in_time` | body | `number` | yes | Clock-in time as a Unix timestamp. |
| `user` | body | `number` | yes | ID of the user to clock in. |
