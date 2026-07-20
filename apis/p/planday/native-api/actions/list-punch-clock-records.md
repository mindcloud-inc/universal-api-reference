# List Punch Clock Records with Planday

Retrieves punch clock records from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/punchclock/v1.0/punchclockshifts`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Punch Clock Records](https://openapi.planday.com/api/punchclock/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | query | `number` | no |
| `from` | query | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
| `shiftId` | query | `number` | no |
| `to` | query | `string` | yes |
