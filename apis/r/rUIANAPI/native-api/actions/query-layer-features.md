# Query layer features with RUIAN

Retrieves layer features from RUIAN API.

## Endpoint

- **Method:** `GET`
- **Path:** `/{layerId}/query`
- **Base URL:** `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`
- **Official documentation:** [Query layer features](https://developers.arcgis.com/rest/services-reference/enterprise/query-map-service-layer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layerId` | path | `number` | yes | Numeric RUIAN layer ID, for example 0 for ParcelaDefinicniBod. |
| `where` | query | `string` | yes | ArcGIS where clause used to filter returned features. |
| `outFields` | query | `string` | no | Comma-separated field list to include in the response. |
| `returnGeometry` | query | `boolean` | no | Return feature geometries in addition to attributes. |
| `resultRecordCount` | query | `number` | no | Maximum number of rows to return. |
