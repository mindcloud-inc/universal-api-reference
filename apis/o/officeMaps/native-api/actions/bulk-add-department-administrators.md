# Bulk Add Department Administrators with OfficeMaps

Adds multiple administrators to a department in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/department/:departmentId/administrators`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Bulk Add Department Administrators](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `operations[]` | body | `array<object>` | yes | People to apply in the bulk request. |
