# Get process versions with YepCode

Retrieves process version records from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/processes/:processId/versions`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get process versions](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processId` | path | `string` | yes | Unique identifier of the process whose versions you want to retrieve. |
