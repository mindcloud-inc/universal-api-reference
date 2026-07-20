# Socialbu: Check Media Upload Status

Retrieves the status of a SocialBu media upload.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/check-media-upload-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/check-media-upload-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/check-media-upload-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "status": "string",
      "upload_token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `status` | string |  |
| `upload_token` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /upload_media/status` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-media-upload-status.md) for the provider-specific parameters and requirements.

