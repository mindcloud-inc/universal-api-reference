# Invidious: Get Popular Videos



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-popular-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-popular-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-popular-videos?${params}`, {
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
      "author": "string",
      "authorId": "string",
      "lengthSeconds": 1,
      "title": "string",
      "videoId": "string",
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorId` | string |  |
| `lengthSeconds` | number |  |
| `title` | string |  |
| `videoId` | string |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /popular` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-popular-videos.md) for the provider-specific parameters and requirements.

