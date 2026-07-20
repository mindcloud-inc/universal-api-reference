# Update Position with Aqara Home for KR

Updates an existing position in Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [Update Position](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `positionId` | body | `string` | yes | Position ID. |
| `positionName` | body | `string` | yes | Position name. |
| `description` | body | `string` | no | Position description. |
