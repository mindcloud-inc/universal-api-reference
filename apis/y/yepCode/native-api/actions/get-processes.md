# Get processes with YepCode

Retrieves a list of processes from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/processes`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get processes](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcesses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Search keywords applied to process name or description. |
