# Update Position Timezone with Aqara Home for KR

Updates a top-level position timezone in Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [Update Position Timezone](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `positionId` | body | `string` | no | Top-level position ID. |
| `timeZone` | body | `string` | no | Timezone in the format GMT+08:00. |
