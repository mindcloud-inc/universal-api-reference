# List Positions with Aqara Home for KR

Retrieves subordinate positions in Aqara Home for KR.

## Endpoint

- **Method:** `POST`
- **Path:** `v3.0/open/api`
- **Base URL:** `https://open-kr.aqara.com`
- **Official documentation:** [List Positions](https://opendoc.aqara.com/en/docs/developmanual/apiDocument/PositionManagement.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentPositionId` | body | `string` | no | Parent position ID. Leave empty to query all positions under the user or project. |
| `pageNum` | body | `number` | no | Page number. Default is 1. |
| `pageSize` | body | `number` | no | Number of items per page. Default is 30. |
