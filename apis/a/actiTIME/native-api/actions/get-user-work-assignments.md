# Get User Work Assignments with actiTIME

Retrieves a user's work assignments from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:uid/workAssignments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get User Work Assignments](https://www.actitime.com/api-documentation/users-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | User ID or username. |
