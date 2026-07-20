# Get execution logs with YepCode

Retrieves execution log entries from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/executions/:id/logs`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get execution logs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/getExecutionLogs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the execution to get logs for. |
