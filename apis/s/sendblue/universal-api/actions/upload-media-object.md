# Sendblue: Upload Media Object

Uploads a media object to Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/upload-media-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/upload-media-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://httpbin.org/image/png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/upload-media-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://httpbin.org/image/png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaUrl` | string | yes | Public URL of the media to upload. Example: `https://httpbin.org/image/png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediaObjectId": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediaObjectId` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/upload-media-object` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media-object.md) for the provider-specific parameters and requirements.

