# Create Bar Chart (Zapier) with ChartLy

Creates a Zapier-friendly bar chart in Chartly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/zapier/bar-chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Create Bar Chart (Zapier)](https://docs.chartly.dev/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Chart title |
| `labels` | body | `string` | yes | Comma-separated labels |
| `values` | body | `string` | yes | Comma-separated numeric values |
| `color` | body | `string` | no | Bar color in hex |
| `width` | body | `number` | no | Chart width in pixels |
| `height` | body | `number` | no | Chart height in pixels |
| `format` | body | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | body | `string` | no | Background color |
| `showLegend` | body | `boolean` | no | Show legend |
| `showGrid` | body | `boolean` | no | Show grid lines |
