# Get Position Details with Aqara Home for KR

Retrieves position details from Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [Get Position Details](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `positionIds[]` | body | `array<string>` | yes | Position ID array. Maximum 50 values. |
