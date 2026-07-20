# Render Chart From URL with ChartLy

Renders a chart image from URL-encoded config in Chartly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chart`
- **Base URL:** `https://api.chartly.dev`
- **Official documentation:** [Render Chart From URL](https://docs.chartly.dev/api#get-v1chart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chart` | query | `string` | yes | Chart.js config as JSON string |
| `width` | query | `number` | yes | Image width in pixels |
| `height` | query | `number` | yes | Image height in pixels |
| `format` | query | `string` | no | Output format Accepted values: `0`, `1`. |
| `backgroundColor` | query | `string` | no | CSS background color |
