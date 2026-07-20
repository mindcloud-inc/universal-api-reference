# Felt: List Map Layers

Retrieves map layers from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layers?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-map-layers?${params}`, {
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
      "attributes": [
        {}
      ],
      "caption": "string",
      "geometry_type": "string",
      "hide_from_legend": true,
      "id": "string",
      "links": {},
      "metadata": {},
      "name": "Ava Chen",
      "progress": 1,
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
| `attributes` | array<object> |  |
| `caption` | string |  |
| `geometry_type` | string |  |
| `hide_from_legend` | boolean |  |
| `id` | string |  |
| `links` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `progress` | number |  |
| `refresh_period` | string |  |
| `status` | string |  |
| `style` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/layers` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-map-layers.md) for the provider-specific parameters and requirements.

