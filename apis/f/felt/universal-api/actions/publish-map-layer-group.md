# Felt: Publish Map Layer Group

Publishes a map layer group to Felt's library.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "layerGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/publish-map-layer-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "layerGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map where the layer group is located. |
| `layerGroupId` | string | yes | The ID of the layer group to publish. |
| `name` | string | no | The name to publish the layer group under. |

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
| `id` | string | Published layer group ID. |
| `layers` | array<object> | Layers included in the published group. |
| `legend_visibility` | string | Legend visibility setting. |
| `name` | string | Published layer group name. |
| `ordering_key` | number | Sort order key. |
| `type` | string | Resource type. |
| `visibility_interaction` | string | Legend interaction behavior. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/layer_groups/:layerGroupId/publish` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-map-layer-group.md) for the provider-specific parameters and requirements.

