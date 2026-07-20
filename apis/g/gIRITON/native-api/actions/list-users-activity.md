# List Users Activity with GIRITON

Retrieves user attendance activity for a selected GIRITON day.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendance/usersActivity`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Users Activity](https://rest.giriton.com/apidoc/#/Attendance/getUsersActivity)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Day to inspect in GIRITON's documented string date format (YYYY-MM-DD). |
| `personIds` | query | `string` | no | Comma-separated database IDs of persons. |
