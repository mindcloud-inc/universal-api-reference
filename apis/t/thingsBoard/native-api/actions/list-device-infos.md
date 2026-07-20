# List Device Infos with ThingsBoard

Retrieves device info records from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/deviceInfos/all`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Device Infos](https://thingsboard.cloud/swagger-ui/index.html#/device-controller/getAllDeviceInfos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | yes | Maximum number of device info records to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
