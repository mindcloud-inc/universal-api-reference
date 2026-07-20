# Felt: List Map Layer Groups

Retrieves map layer groups from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layer-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layer-groups?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layer-groups?${params}`, {
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
| `mapId` | string | yes | The Felt map ID. |

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
      "links": {},
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
| `caption` | string |  |
| `id` | string |  |
| `layers` | array<object> |  |
| `legend_visibility` | string |  |
| `links` | object |  |
| `name` | string |  |
| `ordering_key` | number |  |
| `type` | string |  |
| `visibility_interaction` | string |  |

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/layer_groups` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-map-layer-groups.md) for the provider-specific parameters and requirements.

