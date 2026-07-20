# Get Current Team Member with Zoho WorkDrive

Retrieves the current team member from Zoho WorkDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/teams/:teamId/currentuser`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get Current Team Member](https://workdrive.zoho.com/apidocs/v1/teams/getcurrentteammember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The WorkDrive team ID. |
