# Generate Astrology Data with BodyGraph

Retrieves astrology chart data from BodyGraph.

## Endpoint

- **Method:** `GET`
- **Path:** `/v240815/astro-data`
- **Base URL:** `https://api.bodygraphchart.com`
- **Official documentation:** [Generate Astrology Data](https://bodygraph.com/docs/#generate-astrology-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Local date of birth. Format: Y-M-D H:I |
| `timezone` | query | `string` | yes | Timezone of place of birth. |
| `latitude` | query | `string` | yes | Latitude of place of birth. |
| `longitude` | query | `string` | yes | Longitude of place of birth. |
| `house_system` | query | `string` | yes | House system code, for example W for whole sign or P for Placidus. |
| `design` | query | `string` | no | Exact chart design title from your Chart Designs dashboard. Adds SVG output when provided. |
| `language` | query | `string` | no | Exact language title from your Chart Content tool for localized output. |
