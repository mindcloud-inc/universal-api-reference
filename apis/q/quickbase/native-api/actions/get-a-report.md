# Get a Report with Quickbase

Retrieves a Quickbase report by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/reports/:reportId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Get a Report](https://developer.quickbase.com/operation/getReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `reportId` | path | `string` | yes | The Quickbase report identifier. |
