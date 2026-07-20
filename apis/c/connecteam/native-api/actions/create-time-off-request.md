# Create Time Off Request with Connecteam

Create a new time-off request for a user under a specified policy. The time-off request can be either in pending or approved status.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-off/v1/requests`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Create Time Off Request](https://developer.connecteam.com/reference/post_time_off_request_time_off_v1_requests_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `timeClockId` | body | `number` | no |
| `userId` | body | `number` | yes |
| `policyTypeId` | body | `string` | yes |
| `isAllDay` | body | `boolean` | yes |
| `startDate` | body | `string` | yes |
| `endDate` | body | `string` | yes |
| `startTime` | body | `string` | no |
| `endTime` | body | `string` | no |
| `timezone` | body | `string` | yes |
| `status` | body | `string` | yes |
| `employeeNote` | body | `string` | no |
| `managerNote` | body | `string` | no |
| `isAdjustForDayLightSaving` | body | `boolean` | no |
