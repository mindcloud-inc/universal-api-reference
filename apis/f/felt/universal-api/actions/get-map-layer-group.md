# Felt: Get Map Layer Group

Retrieves a map layer group from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-layer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-layer-group?connectionId=$CONNECTION_ID&mapId=string&layerGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string",
  "layerGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-map-layer-group?${params}`, {
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
| `mapId` | string | yes | The ID of the map. |
| `layerGroupId` | string | yes | The ID of the layer group. |

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

Through the native Felt API, this operation is `GET /maps/:mapId/layer_groups/:layerGroupId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-layer-group.md) for the provider-specific parameters and requirements.

