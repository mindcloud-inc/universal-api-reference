# Change Request Status with BambooHR

Updates a time off request status in BambooHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/time_off/requests/:requestId/status`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Change Request Status](https://documentation.bamboohr.com/reference/time-off-change-a-request-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The BambooHR time-off request identifier to update. |
