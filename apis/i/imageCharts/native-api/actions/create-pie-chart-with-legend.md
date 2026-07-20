# Create Pie Chart With Legend with Image-Charts

Creates a pie chart with a legend with Image-Charts.

## Endpoint

- **Method:** `GET`
- **Path:** `/chart`
- **Base URL:** `https://image-charts.com`
- **Official documentation:** [Create Pie Chart With Legend](https://documentation.image-charts.com/pie-charts/#pie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chs` | query | `string` | yes | Chart size in pixels, for example 300x200. |
| `chd` | query | `string` | yes | Chart data in Image-Charts format. |
| `chdl` | query | `string` | yes | Legend entries separated by pipes. |
