# Generate HD Data with BodyGraph

Retrieves Human Design chart data from BodyGraph.

## Endpoint

- **Method:** `GET`
- **Path:** `/v221006/hd-data`
- **Base URL:** `https://api.bodygraphchart.com`
- **Official documentation:** [Generate HD Data](https://bodygraph.com/docs/#generate-hd-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Local date of birth. Format: Y-M-D H:I |
| `timezone` | query | `string` | yes | Timezone of place of birth. |
| `design` | query | `string` | no | Exact chart design title from your Chart Designs dashboard. Adds SVG output when provided. |
| `language` | query | `string` | no | Exact language title from your Chart Content tool for localized output. |
