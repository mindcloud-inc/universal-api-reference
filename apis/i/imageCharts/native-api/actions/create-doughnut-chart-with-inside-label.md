# Create Doughnut Chart With Inside Label with Image-Charts

Creates a doughnut chart with an inside label using Image-Charts.

## Endpoint

- **Method:** `GET`
- **Path:** `/chart`
- **Base URL:** `https://image-charts.com`
- **Official documentation:** [Create Doughnut Chart With Inside Label](https://documentation.image-charts.com/pie-charts/#inside-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chs` | query | `string` | yes | Chart size in pixels, for example 300x200. |
| `chd` | query | `string` | yes | Chart data in Image-Charts format. |
| `chl` | query | `string` | yes | Slice labels separated by pipes. |
| `chdl` | query | `string` | yes | Legend entries separated by pipes. |
| `chli` | query | `string` | yes | Label shown inside the doughnut chart. |
