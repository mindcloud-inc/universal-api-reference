# Render Chart From JSON with ChartLy

Renders a chart image from JSON config in Chartly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Render Chart From JSON](https://docs.chartly.dev/api#post-v1chart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chart` | body | `string` | yes | Chart.js config as JSON string |
| `width` | body | `number` | yes | Image width in pixels |
| `height` | body | `number` | yes | Image height in pixels |
| `format` | body | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | body | `string` | no | CSS background color |
