# Bulk Add Department Members with OfficeMaps

Adds multiple members to a department in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/department/:departmentId/members`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Bulk Add Department Members](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `operations[]` | body | `array<object>` | yes | People to apply in the bulk request. |
