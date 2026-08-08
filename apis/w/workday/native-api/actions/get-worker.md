# Get Worker with Workday

Get a single worker from Workday Time Tracking by Workday worker ID.

## Endpoint

- **Method:** `GET`
- **Path:** `workers/:ID`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [Get Worker](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | The Workday ID of the worker. Use a returned id from Get Workers. |
