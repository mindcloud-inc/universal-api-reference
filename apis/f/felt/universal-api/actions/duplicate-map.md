# Felt: Duplicate Map

Creates a duplicate of a map in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The Felt map ID. |
| `title` | string | no | Title for the duplicated map. |
| `destination` | object | no | Destination object with either project_id or folder_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basemap": "string",
      "elements": {},
      "id": "string",
      "layer_groups": [
        {}
      ],
      "layers": [
        {}
      ],
      "project_id": "string",
      "public_access": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basemap` | string |  |
| `elements` | object |  |
| `id` | string |  |
| `layer_groups` | array<object> |  |
| `layers` | array<object> |  |
| `project_id` | string |  |
| `public_access` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/duplicate` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-map.md) for the provider-specific parameters and requirements.

