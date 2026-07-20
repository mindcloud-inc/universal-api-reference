# Tolstoy: List Videos

Retrieves all video records from Tolstoy.

```
GET https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolstoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos?${params}`, {
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
      "videos": [
        {
          "createdAt": "string",
          "gifSize": "string",
          "gifUrl": "https://example.com",
          "id": "string",
          "name": "Ava Chen",
          "posterGifUrl": "https://example.com",
          "videoUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videos` | array<object> | List of Tolstoy videos |
| `videos[].createdAt` | string | Creation timestamp |
| `videos[].gifSize` | string | GIF size metadata |
| `videos[].gifUrl` | string | Generated GIF URL |
| `videos[].id` | string | Tolstoy video id |
| `videos[].name` | string | Video name |
| `videos[].posterGifUrl` | string | Generated poster GIF URL |
| `videos[].videoUrl` | string | Hosted source video URL |

## Native endpoint

Through the native Tolstoy API, this operation is `GET /videos/videos` (base URL `https://api.gotolstoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.

