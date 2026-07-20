# Bulk Remove Department Managers with OfficeMaps

Removes multiple managers from a department in OfficeMaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/department/:departmentId/managers`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Bulk Remove Department Managers](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `operations[]` | body | `array<object>` | yes | People to apply in the bulk request. |
