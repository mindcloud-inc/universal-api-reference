# List Alarm Types with ThingsBoard

Retrieves available alarm types from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/alarm/types`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Alarm Types](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/getAlarmTypes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | yes | Maximum number of alarm types to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
