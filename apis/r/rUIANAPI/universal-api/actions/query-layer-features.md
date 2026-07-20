# RUIAN: Query layer features

Retrieves layer features from RUIAN API.

```
GET https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/query-layer-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RUIAN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/query-layer-features?connectionId=$CONNECTION_ID&layerId=0&where=1%3D1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerId": "0",
  "where": "1=1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rUIANAPI/latest/actions/query-layer-features?${params}`, {
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
| `layerId` | number | yes | Numeric RUIAN layer ID, for example 0 for ParcelaDefinicniBod. Example: `0`. |
| `where` | string | yes | ArcGIS where clause used to filter returned features. Default: `1=1`. Example: `1=1`. |
| `outFields` | string | no | Comma-separated field list to include in the response. Default: `*`. Example: `*`. |
| `returnGeometry` | boolean | no | Return feature geometries in addition to attributes. |
| `resultRecordCount` | number | no | Maximum number of rows to return. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayFieldName": "Ava Chen",
      "exceededTransferLimit": true,
      "features": [
        {}
      ],
      "fieldAliases": {},
      "fields": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayFieldName` | string |  |
| `exceededTransferLimit` | boolean |  |
| `features` | array<object> |  |
| `fieldAliases` | object |  |
| `fields` | array<object> |  |

## Native endpoint

Through the native RUIAN API, this operation is `GET /{layerId}/query` (base URL `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-layer-features.md) for the provider-specific parameters and requirements.

