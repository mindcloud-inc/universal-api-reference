# Add Chart with Clappia

Creates a new chart in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/addChart`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add Chart](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `chartIndex` | body | `number` | yes | Zero-based chart index where the new chart should be inserted. |
| `chartType` | body | `string` | yes | Chart type, such as barGraph. |
| `chartTitle` | body | `string` | no | Display title for the chart. |
| `width` | body | `number` | no | Chart width percentage. |
| `isStacked` | body | `boolean` | no | Whether the chart should be stacked. |
| `direction` | body | `string` | no | Chart direction, such as Horizontal or Vertical. |
| `aggregationDimensions[]` | body | `array<object>` | yes | Aggregation dimension objects that define the chart metrics. |
| `dimensions[]` | body | `array<object>` | no | Dimension objects that define the chart grouping axes. |
