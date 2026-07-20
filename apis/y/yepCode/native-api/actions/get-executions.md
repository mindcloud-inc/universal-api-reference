# Get executions with YepCode

Retrieves a list of executions from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/executions`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get executions](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/getExecutions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Search keywords applied to process name or execution comment. |
| `processId` | query | `string` | no | Filter executions by process ID. |
| `status` | query | `string` | no | Filter executions by status. |
| `from` | query | `date` | no | Filter executions created from this date and time. |
| `to` | query | `date` | no | Filter executions created until this date and time. |
| `comment` | query | `string` | no | Filter executions by comment text. |
