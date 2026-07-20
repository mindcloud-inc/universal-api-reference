# Bulk Remove Department Administrators with OfficeMaps

Removes multiple administrators from a department in OfficeMaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/department/:departmentId/administrators`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Bulk Remove Department Administrators](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `operations[]` | body | `array<object>` | yes | People to apply in the bulk request. |
