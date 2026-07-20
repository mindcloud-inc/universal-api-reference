# City of Beverly Hills: Get Feature Service

Retrieves feature service details from City of Beverly Hills.

```
GET https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Beverly Hills `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-service?connectionId=$CONNECTION_ID&serviceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/get-feature-service?${params}`, {
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
| `serviceName` | string | yes | ArcGIS service folder or service name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentVersion": 1,
      "layers": [
        [
          {}
        ]
      ],
      "serviceItemId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentVersion` | number | ArcGIS REST API version for the feature service response. |
| `layers[]` | array<object> | Layer summaries returned by the feature service. |
| `layers[].id` | number | Layer id. |
| `layers[].name` | string | Layer name. |
| `layers[].type` | string | Layer type. |
| `serviceItemId` | string | ArcGIS item id for the feature service. |

## Native endpoint

Through the native City of Beverly Hills API, this operation is `GET :serviceName/FeatureServer` (base URL `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-service.md) for the provider-specific parameters and requirements.

