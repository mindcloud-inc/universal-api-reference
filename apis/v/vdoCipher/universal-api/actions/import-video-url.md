# VdoCipher: Import Video URL

Imports a video from a URL into VdoCipher.

```
POST https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/import-video-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/import-video-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/import-video-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "length": "string",
      "poster": "string",
      "public": "string",
      "status": "string",
      "title": "string",
      "upload_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `length` | string |  |
| `poster` | string |  |
| `public` | string |  |
| `status` | string |  |
| `title` | string |  |
| `upload_time` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `PUT /videos/importUrl` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-video-url.md) for the provider-specific parameters and requirements.

