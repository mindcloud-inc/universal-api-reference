# Remove Department Administrator with OfficeMaps

Removes an administrator from a department in OfficeMaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/department/:departmentId/administrator/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Remove Department Administrator](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
