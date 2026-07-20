# Get scheduled processes with YepCode

Retrieves a list of scheduled processes from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get scheduled processes](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/getSchedules)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processId` | query | `string` | no | Filter scheduled processes by process ID. |
| `keywords` | query | `string` | no | Filter scheduled processes by process name or schedule comment keywords. |
