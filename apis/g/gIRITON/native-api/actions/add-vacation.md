# Add Vacation with GIRITON

Creates a new vacation entry in GIRITON.

## Endpoint

- **Method:** `POST`
- **Path:** `/attendance/vacation`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Add Vacation](https://rest.giriton.com/apidoc/#/Attendance/addVacation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `string` | yes | Starting date of vacation. |
| `userEmail` | body | `string` | no | User email address for the vacation. |
| `userId` | body | `string` | no | User ID for the vacation. |
| `userNumber` | body | `string` | no | User number for the vacation. |
| `dateTo` | body | `string` | yes | Last date of vacation. |
