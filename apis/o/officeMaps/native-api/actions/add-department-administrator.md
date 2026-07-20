# Add Department Administrator with OfficeMaps

Adds an administrator to a department in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/department/:departmentId/administrator/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Add Department Administrator](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
