# Get Member Attendance with Virtually

Retrieves a member's attendance from Virtually.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgId/members/:memberId/attendance`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Get Member Attendance](https://app.tryvirtually.com/api/docs#/Members/MembersController_getMemberAttendance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The member ID. |
