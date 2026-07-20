# Create TOIL Accrual with RotaCloud

Creates a toil accrual record in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/toil_accruals`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create TOIL Accrual](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `durationHours` | body | `number` | yes | TOIL duration in hours. |
| `leaveYear` | body | `number` | yes | Leave year for the accrual. |
| `userId` | body | `number` | yes | User receiving the accrual. |
