# Felt: Publish Map Layer

Publishes a map layer to Felt's library.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "layerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "layerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map where the layer is located. |
| `layerId` | string | yes | The ID of the layer to publish. |
| `name` | string | no | The name to publish the layer under. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "geometry_type": "string",
      "id": "string",
      "legend_visibility": "string",
      "name": "Ava Chen",
      "ordering_key": 1,
      "refresh_period": "string",
      "status": "string",
      "style": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string | Layer caption. |
| `geometry_type` | string | Layer geometry type. |
| `id` | string | Published library layer ID. |
| `legend_visibility` | string | Legend visibility setting. |
| `name` | string | Published layer name. |
| `ordering_key` | number | Sort order key. |
| `refresh_period` | string | Refresh interval. |
| `status` | string | Processing status. |
| `style` | object | Felt Style Language style definition. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/layers/:layerId/publish` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-map-layer.md) for the provider-specific parameters and requirements.

