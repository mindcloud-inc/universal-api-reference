# List Alarms with ThingsBoard

Retrieves alarms for a specific entity from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/alarm/:entityType/:entityId`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Alarms](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/getAlarms)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | path | `string` | yes | The ThingsBoard entity ID. |
| `pageSize` | query | `number` | yes | Maximum number of alarms to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
