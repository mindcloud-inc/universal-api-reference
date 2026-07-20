# Felt: Update Map Layer Group

Updates an existing map layer group in Felt.

```
PUT https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-map-layer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-map-layer-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "layerGroupId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/update-map-layer-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "layerGroupId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map. |
| `layerGroupId` | string | yes | The ID of the layer group. |
| `name` | string | yes | Updated layer group name. |
| `caption` | string | no | Updated layer group caption. |
| `legendVisibility` | list | no | Controls whether the layer group appears in the legend. One of: `0`, `1`. |
| `visibilityInteraction` | list | no | Controls how the layer group appears in the legend. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "id": "string",
      "layers": [
        {}
      ],
      "legend_visibility": "string",
      "name": "Ava Chen",
      "ordering_key": 1,
      "type": "string",
      "visibility_interaction": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string | Layer group caption. |
| `id` | string | Layer group ID. |
| `layers` | array<object> | Layers contained in the group. |
| `legend_visibility` | string | Legend visibility setting. |
| `name` | string | Layer group name. |
| `ordering_key` | number | Sort order key. |
| `type` | string | Resource type. |
| `visibility_interaction` | string | Legend interaction behavior. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/layer_groups/:layerGroupId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-map-layer-group.md) for the provider-specific parameters and requirements.

