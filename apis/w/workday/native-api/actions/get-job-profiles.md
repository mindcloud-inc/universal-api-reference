# Get Job Profiles with Workday

## Endpoint

- **Method:** `GET`
- **Path:** `jobProfiles/:ID`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [Get Job Profiles](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | The Workday ID of the job. Use a returned id from Get Jobs. |
