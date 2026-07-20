# List Intent with Zoominfo

Finds intent-based companies and contacts in ZoomInfo.

## Endpoint

- **Method:** `POST`
- **Path:** `search/intent`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [List Intent](https://api-docs.zoominfo.com/#93f940a4-4381-49dd-8fbc-42cbc75a7a39)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topics[]` | body | `array<string>` | yes | Send multiple values as a array. |
| `signalScoreMin` | body | `number` | no | Minimum signal score. |
| `signalScoreMax` | body | `number` | no | Maximum signal score. |
| `audienceStrengthMin` | body | `string` | no | Minimum audience strength score. |
| `audienceStrengthMax` | body | `string` | no | Maximum audience strength score. |
| `metroRegion` | body | `string` | no | Company metro area. |
| `industryCodes` | body | `string` | no | Top-level industry codes. |
| `sortBy` | body | `string` | no | Sort results by a valid output field. |
| `sortOrder` | body | `string` | no | Sort direction. |
