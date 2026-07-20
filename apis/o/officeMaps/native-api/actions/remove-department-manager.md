# Remove Department Manager with OfficeMaps

Removes a manager from a department in OfficeMaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/department/:departmentId/manager/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Remove Department Manager](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
