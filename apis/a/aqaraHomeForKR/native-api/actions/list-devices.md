# List Devices with Aqara Home for KR

Retrieves devices from Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [List Devices](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/DeviceManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dids[]` | body | `array<string>` | no | Device ID array. Up to 100 device IDs can be queried at a time. |
| `positionId` | body | `string` | no | Position ID. Leave empty to query all devices under the user. |
| `pageNum` | body | `number` | no | Page number. Default is 1. |
| `pageSize` | body | `number` | no | Number of items per page. Default is 50. |
