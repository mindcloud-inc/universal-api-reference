# Add Department Manager with OfficeMaps

Adds a manager to a department in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/department/:departmentId/manager/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Add Department Manager](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
