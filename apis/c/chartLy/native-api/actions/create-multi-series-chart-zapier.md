# Create Multi-Series Chart (Zapier) with ChartLy

Creates a Zapier-friendly multi-series chart in Chartly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/zapier/multi-series-chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Create Multi-Series Chart (Zapier)](https://docs.chartly.dev/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Chart title |
| `labels` | body | `string` | yes | Comma-separated labels |
| `chartType` | body | `string` | no | Chart type Accepted values: `0`, `1`. |
| `series1_name` | body | `string` | yes | First series name |
| `series1_values` | body | `string` | yes | First series values (comma-separated) |
| `series1_color` | body | `string` | no | First series color |
| `series2_name` | body | `string` | no | Second series name |
| `series2_values` | body | `string` | no | Second series values (comma-separated) |
| `series2_color` | body | `string` | no | Second series color |
| `series3_name` | body | `string` | no | Third series name |
| `series3_values` | body | `string` | no | Third series values (comma-separated) |
| `series3_color` | body | `string` | no | Third series color |
| `width` | body | `number` | no | Chart width in pixels |
| `height` | body | `number` | no | Chart height in pixels |
| `format` | body | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | body | `string` | no | Background color |
| `showLegend` | body | `boolean` | no | Show legend |
| `showGrid` | body | `boolean` | no | Show grid lines |
