# Felt: Update Layer Style

Updates a map layer style in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-layer-style
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-layer-style" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "layerId": "string",
  "style": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-layer-style', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "layerId": "string",
    "style": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map where the layer is located. |
| `layerId` | string | yes | The ID of the layer to update. |
| `style` | object | yes | The new layer style in Felt Style Language format. |

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
| `id` | string | Layer ID. |
| `legend_visibility` | string | Legend visibility setting. |
| `name` | string | Layer name. |
| `refresh_period` | string | Refresh interval. |
| `status` | string | Processing status. |
| `style` | object | Felt Style Language style definition. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/layers/:layerId/update_style` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-layer-style.md) for the provider-specific parameters and requirements.

