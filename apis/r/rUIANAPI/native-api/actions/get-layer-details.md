# Get layer details with RUIAN

Retrieves layer details from RUIAN API.

## Endpoint

- **Method:** `GET`
- **Path:** `/{layerId}`
- **Base URL:** `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`
- **Official documentation:** [Get layer details](https://developers.arcgis.com/rest/services-reference/enterprise/layer-table/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layerId` | path | `number` | yes | Numeric RUIAN layer ID, for example 0 for ParcelaDefinicniBod. |
