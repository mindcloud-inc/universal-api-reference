# Query Features with City of Beverly Hills

Queries layer features in City of Beverly Hills by service and layer.

## Endpoint

- **Method:** `GET`
- **Path:** `:serviceName/FeatureServer/:layerId/query`
- **Base URL:** `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`
- **Official documentation:** [Query Features](https://developers.arcgis.com/rest/services-reference/enterprise/query-feature-service-layer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cacheHint` | query | `boolean` | no | Hint that the server may cache the query. |
| `datumTransformation` | query | `string` | no | Datum transformation used when projecting geometries. |
| `defaultSR` | query | `string` | no | Default spatial reference for the request. |
| `distance` | query | `number` | no | Buffer distance used with geometry-based queries. |
| `fullText` | query | `string` | no | Full text search term. |
| `geometry` | query | `string` | no | Spatial filter geometry payload. |
| `geometryPrecision` | query | `number` | no | Decimal places for returned geometries. |
| `geometryType` | query | `string` | no | The type of geometry supplied with the spatial filter. |
| `inSR` | query | `string` | no | Input spatial reference for geometry filters. |
| `layerId` | path | `string` | yes | Layer identifier within the FeatureServer. |
| `maxAllowableOffset` | query | `number` | no | Generalization offset for returned geometries. |
| `orderByFields` | query | `string` | no | Comma-separated field list for ordering results. |
| `outFields` | query | `string` | no | Comma-separated list of fields to return. |
| `outSR` | query | `string` | no | Output spatial reference for returned geometry. |
| `resultOffset` | query | `number` | no | Number of features to skip before returning results. |
| `resultRecordCount` | query | `number` | no | Maximum number of features to return. |
| `resultType` | query | `string` | no | Controls the query result mode. |
| `returnCentroid` | query | `boolean` | no | Return the geometry centroid for each feature. |
| `returnCountOnly` | query | `boolean` | no | Return only the feature count. |
| `returnDistinctValues` | query | `boolean` | no | Return distinct values for the requested fields. |
| `returnEnvelope` | query | `boolean` | no | Return the geometry envelope for each feature. |
| `returnExceededLimitFeatures` | query | `boolean` | no | Return features even when the transfer limit is exceeded. |
| `returnExtentOnly` | query | `boolean` | no | Return only the query extent. |
| `returnGeometry` | query | `boolean` | no | Include geometry in each feature. |
| `returnIdsOnly` | query | `boolean` | no | Return only object IDs. |
| `returnM` | query | `boolean` | no | Include m-values in returned geometries. |
| `returnTrueCurves` | query | `boolean` | no | Return true curves in output geometries. |
| `returnZ` | query | `boolean` | no | Include z-values in returned geometries. |
| `serviceName` | path | `string` | yes | ArcGIS service folder or service name. |
| `spatialRel` | query | `string` | no | Spatial relationship used with geometry filters. |
| `sqlFormat` | query | `string` | no | SQL dialect for the where clause. |
| `units` | query | `string` | no | Units for the buffer distance. |
| `where` | query | `string` | no | ArcGIS SQL where clause. |
