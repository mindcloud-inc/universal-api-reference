# Flotiq: Upload Media

Uploads a media file to Flotiq.

```
POST https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/upload-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/upload-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/upload-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The media file to upload. |
| `type` | list | yes | The uploaded media type: image or file. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "extension": "string",
      "externalId": "string",
      "fileName": "Ava Chen",
      "height": 1,
      "id": "string",
      "internal": {},
      "mimeType": "string",
      "size": 1,
      "source": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "variants": [
        {}
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `extension` | string |  |
| `externalId` | string |  |
| `fileName` | string |  |
| `height` | number |  |
| `id` | string |  |
| `internal` | object |  |
| `mimeType` | string |  |
| `size` | number |  |
| `source` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `variants` | array<object> |  |
| `width` | number |  |

## Native endpoint

Through the native Flotiq API, this operation is `POST https://api.flotiq.com/api/media` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media.md) for the provider-specific parameters and requirements.

