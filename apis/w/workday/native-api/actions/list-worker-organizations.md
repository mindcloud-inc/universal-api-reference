# List Worker Organizations with Workday

## Endpoint

- **Method:** `GET`
- **Path:** `workers/:ID/organizations`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [List Worker Organizations](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers/-ID-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | The Workday ID of the worker. Use a returned id from Get Workers. |
