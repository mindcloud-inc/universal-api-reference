# List Closed Attendance with GIRITON

Retrieves closed attendance records for a selected GIRITON month.

## Endpoint

- **Method:** `GET`
- **Path:** `/attendance/closedAttendance`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Closed Attendance](https://rest.giriton.com/apidoc/#/Attendance/getClosedAttendance)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | yes | Required month of the queried period, for example 2022-01. |
