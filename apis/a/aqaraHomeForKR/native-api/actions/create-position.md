# Create Position with Aqara Home for KR

Creates a new position in Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [Create Position](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `positionName` | body | `string` | yes | Position name. |
| `description` | body | `string` | no | Position description. |
| `parentPositionId` | body | `string` | no | Parent position ID. Leave empty to create a top-level location. |
