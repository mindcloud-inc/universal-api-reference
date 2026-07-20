# Get process with YepCode

Retrieves details for a process from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/processes/:identifier`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Unique identifier of the process to retrieve. You can use either the process UUID or slug. |
