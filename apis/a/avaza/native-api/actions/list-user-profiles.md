# List User Profiles with Avaza

Retrieves user profiles from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/UserProfile`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List User Profiles](https://api.avaza.com/#!/UserProfile/UserProfile_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Roles` | query | `string` | no | Optional list of comma separated role codes to filter users by (e.g. "TimesheetUser,Admin") |
| `Tags` | query | `string` | no | — |
| `CurrentUserOnly` | query | `boolean` | no | Optional boolean (true/false) to filter to only show current authenticated user (always true for non Admin/Finance Manager users) |
| `CompanyIDFK` | query | `number` | no | Optionally filter by Company ID |
| `Email` | query | `string` | no | Optionally filter by user email address |
