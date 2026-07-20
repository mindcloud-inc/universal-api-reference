# Add Department Member with OfficeMaps

Adds a member to a department in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/department/:departmentId/member/:personId`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Add Department Member](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Department UUID. |
| `personId` | path | `string` | yes | Person UUID. |
