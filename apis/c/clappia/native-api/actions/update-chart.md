# Update Chart with Clappia

Updates an existing chart in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/updateChart`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Chart](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `chartIndex` | body | `number` | yes | Zero-based chart index to update. |
| `chartTitle` | body | `string` | no | Updated display title for the chart. |
| `width` | body | `number` | no | Updated chart width percentage. |
| `isStacked` | body | `boolean` | no | Whether the updated chart should be stacked. |
| `direction` | body | `string` | no | Updated chart direction, such as Horizontal or Vertical. |
| `aggregationDimensions[]` | body | `array<object>` | no | Updated aggregation dimension objects for the chart metrics. |
| `dimensions[]` | body | `array<object>` | no | Updated dimension objects for the chart grouping axes. |
