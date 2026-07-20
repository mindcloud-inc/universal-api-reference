# Remove Department Member with OfficeMaps

Removes a member from a department in OfficeMaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/department/:departmentId/member/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Remove Department Member](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
