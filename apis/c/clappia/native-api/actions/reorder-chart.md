# Reorder Chart with Clappia

Updates chart display order in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/reorderChart`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Reorder Chart](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `sourceChartIndex` | body | `number` | yes | Zero-based chart index to move from. |
| `targetChartIndex` | body | `number` | yes | Zero-based chart index to move to. |
