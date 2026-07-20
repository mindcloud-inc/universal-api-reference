# Socialbu: Initiate Media Upload

Initiates a media upload to SocialBu.

```
POST https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/initiate-media-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/initiate-media-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/initiate-media-upload', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "signed_url": "https://example.com",
      "status": "string",
      "upload_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `signed_url` | string |  |
| `status` | string |  |
| `upload_token` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `POST /upload_media` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-media-upload.md) for the provider-specific parameters and requirements.

