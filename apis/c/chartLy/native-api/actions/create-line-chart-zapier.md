# Create Line Chart (Zapier) with ChartLy

Creates a Zapier-friendly line chart in Chartly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/zapier/line-chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Create Line Chart (Zapier)](https://docs.chartly.dev/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Chart title |
| `labels` | body | `string` | yes | Comma-separated labels |
| `values` | body | `string` | yes | Comma-separated numeric values |
| `color` | body | `string` | no | Line color in hex |
| `width` | body | `number` | no | Chart width in pixels |
| `height` | body | `number` | no | Chart height in pixels |
| `format` | body | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | body | `string` | no | Background color |
| `fillArea` | body | `boolean` | no | Fill area under the line |
| `showPoints` | body | `boolean` | no | Show data points |
| `tension` | body | `number` | no | Line curve tension from 0 to 1 |
| `showLegend` | body | `boolean` | no | Show legend |
| `showGrid` | body | `boolean` | no | Show grid lines |
