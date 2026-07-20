# Get process version aliases with YepCode

Retrieves process version aliases from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/processes/:processId/aliases`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get process version aliases](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersionAliases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processId` | path | `string` | yes | Process ID whose version aliases you want to retrieve. |
| `versionId` | query | `string` | no | Optionally filter aliases to a specific process version. |
