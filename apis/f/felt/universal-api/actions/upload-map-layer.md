# Felt: Upload Map Layer

Uploads a new map layer to Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/upload-map-layer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/upload-map-layer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/upload-map-layer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | Map ID to upload the new layer to. |
| `name` | string | yes | Display name for the new layer. |
| `importUrl` | string | no | Public URL to geodata to import instead of uploading a file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Optional layer metadata object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "layer_group_id": "string",
      "layer_id": "string",
      "presigned_attributes": {},
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
| `layer_group_id` | string | Created layer group ID. |
| `layer_id` | string | Created layer ID. |
| `presigned_attributes` | object | Presigned upload fields for file uploads when applicable. |
| `type` | string | Upload response type. |
| `url` | string | Presigned upload URL for file uploads when applicable. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/upload` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-map-layer.md) for the provider-specific parameters and requirements.

