# Create Pie Chart (Zapier) with ChartLy

Creates a Zapier-friendly pie chart in Chartly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/zapier/pie-chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Create Pie Chart (Zapier)](https://docs.chartly.dev/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Chart title |
| `labels` | body | `string` | yes | Comma-separated labels |
| `values` | body | `string` | yes | Comma-separated values |
| `colors` | body | `string` | no | Comma-separated colors |
| `width` | body | `number` | no | Chart width in pixels |
| `height` | body | `number` | no | Chart height in pixels |
| `format` | body | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | body | `string` | no | Background color |
| `showLegend` | body | `boolean` | no | Show legend |
| `legendPosition` | body | `string` | no | Legend position Accepted values: `0`, `1`, `2`, `3`. |
