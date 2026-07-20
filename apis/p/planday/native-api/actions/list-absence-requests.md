# List Absence Requests with Planday

Retrieves a list of absence requests from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/absence/v1.0/absencerequests`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Absence Requests](https://openapi.planday.com/api/absence/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | query | `number` | no |
| `endDate` | query | `string` | no |
| `Limit` | query | `number` | no |
| `Offset` | query | `number` | no |
| `startDate` | query | `string` | no |
| `status[]` | query | `array<string>` | no |
