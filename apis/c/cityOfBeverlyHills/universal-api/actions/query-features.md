# City of Beverly Hills: Query Features

Queries layer features in City of Beverly Hills by service and layer.

```
GET https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/query-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Beverly Hills `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/query-features?connectionId=$CONNECTION_ID&layerId=string&serviceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerId": "string",
  "serviceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/query-features?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `geometry` | string | no | Spatial filter geometry payload. |
| `inSR` | string | no | Input spatial reference for geometry filters. |
| `layerId` | string | yes | Layer identifier within the FeatureServer. |
| `orderByFields` | string | no | Comma-separated field list for ordering results. |
| `outFields` | string | no | Comma-separated list of fields to return. Default: `*`. |
| `outSR` | string | no | Output spatial reference for returned geometry. |
| `resultOffset` | number | no | Number of features to skip before returning results. |
| `resultRecordCount` | number | no | Maximum number of features to return. |
| `returnCountOnly` | boolean | no | Return only the feature count. |
| `returnGeometry` | boolean | no | Include geometry in each feature. Default: `true`. |
| `returnIdsOnly` | boolean | no | Return only object IDs. |
| `serviceName` | string | yes | ArcGIS service folder or service name. |
| `spatialRel` | string | no | Spatial relationship used with geometry filters. |
| `where` | string | no | ArcGIS SQL where clause. Default: `1=1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cacheHint` | boolean | no | Hint that the server may cache the query. Default: `false`. |
| `datumTransformation` | string | no | Datum transformation used when projecting geometries. |
| `defaultSR` | string | no | Default spatial reference for the request. |
| `distance` | number | no | Buffer distance used with geometry-based queries. |
| `fullText` | string | no | Full text search term. |
| `geometryPrecision` | number | no | Decimal places for returned geometries. |
| `geometryType` | string | no | The type of geometry supplied with the spatial filter. Default: `esriGeometryEnvelope`. |
| `maxAllowableOffset` | number | no | Generalization offset for returned geometries. |
| `resultType` | string | no | Controls the query result mode. Default: `none`. |
| `returnCentroid` | boolean | no | Return the geometry centroid for each feature. Default: `false`. |
| `returnDistinctValues` | boolean | no | Return distinct values for the requested fields. Default: `false`. |
| `returnEnvelope` | boolean | no | Return the geometry envelope for each feature. Default: `false`. |
| `returnExceededLimitFeatures` | boolean | no | Return features even when the transfer limit is exceeded. Default: `true`. |
| `returnExtentOnly` | boolean | no | Return only the query extent. Default: `false`. |
| `returnM` | boolean | no | Include m-values in returned geometries. Default: `false`. |
| `returnTrueCurves` | boolean | no | Return true curves in output geometries. Default: `false`. |
| `returnZ` | boolean | no | Include z-values in returned geometries. Default: `false`. |
| `sqlFormat` | string | no | SQL dialect for the where clause. Default: `none`. |
| `units` | string | no | Units for the buffer distance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exceededTransferLimit": true,
      "features": [
        [
          {}
        ]
      ],
      "fields": [
        [
          {}
        ]
      ],
      "geometryType": "string",
      "objectIdFieldName": "Ava Chen",
      "spatialReference": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exceededTransferLimit` | boolean | Whether the service truncated the result set. |
| `features[]` | array<object> | Returned feature collection. |
| `features[].attributes` | object | Feature attribute map. |
| `features[].geometry` | object | Feature geometry payload. |
| `fields[]` | array<object> | Query field metadata. |
| `fields[].name` | string | Field name. |
| `geometryType` | string | Geometry type returned by the query. |
| `objectIdFieldName` | string | Object id field name for the query response. |
| `spatialReference` | object | Spatial reference for returned geometries. |

## Native endpoint

Through the native City of Beverly Hills API, this operation is `GET :serviceName/FeatureServer/:layerId/query` (base URL `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-features.md) for the provider-specific parameters and requirements.

