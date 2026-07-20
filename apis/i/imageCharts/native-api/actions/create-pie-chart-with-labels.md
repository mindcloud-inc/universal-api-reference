# Create Pie Chart With Labels with Image-Charts

Creates a labeled pie chart with Image-Charts.

## Endpoint

- **Method:** `GET`
- **Path:** `/chart`
- **Base URL:** `https://image-charts.com`
- **Official documentation:** [Create Pie Chart With Labels](https://documentation.image-charts.com/pie-charts/#pie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chs` | query | `string` | yes | Chart size in pixels, for example 300x200. |
| `chd` | query | `string` | yes | Chart data in Image-Charts format. |
| `chl` | query | `string` | yes | Slice labels separated by pipes. |
