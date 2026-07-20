# City of Beverly Hills: Get Layer

Retrieves feature layer details from City of Beverly Hills.

```
GET https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Beverly Hills `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer?connectionId=$CONNECTION_ID&layerId=string&serviceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layerId": "string",
  "serviceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-layer?${params}`, {
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
| `layerId` | string | yes | Layer identifier within the FeatureServer. |
| `serviceName` | string | yes | ArcGIS service folder or service name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentVersion": 1,
      "fields": [
        [
          {}
        ]
      ],
      "geometryType": "string",
      "id": 1,
      "name": "Ava Chen",
      "objectIdField": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentVersion` | number | ArcGIS REST API version for the layer response. |
| `fields[]` | array<object> | Layer field metadata. |
| `fields[].alias` | string | Field alias. |
| `fields[].name` | string | Field name. |
| `fields[].type` | string | Field type. |
| `geometryType` | string | Geometry type returned by the layer. |
| `id` | number | Layer id. |
| `name` | string | Layer name. |
| `objectIdField` | string | Object id field name. |
| `type` | string | Layer type. |

## Native endpoint

Through the native City of Beverly Hills API, this operation is `GET :serviceName/FeatureServer/:layerId` (base URL `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-layer.md) for the provider-specific parameters and requirements.

