# Planet Money Podcast: List Recent Episodes

Retrieves the latest Planet Money episodes from the NPR RSS feed.

```
GET https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-recent-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planet Money Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-recent-episodes?${params}`, {
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
      "data": {
        "data": [
          1
        ],
        "type": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw XML feed payload returned as a Buffer-like object. |
| `data.data` | array<number> | Byte array containing the raw XML feed response body. |
| `data.type` | string | Node.js buffer marker for the payload container. |
| `success` | boolean | Whether the RSS feed request succeeded. |

## Native endpoint

Through the native Planet Money Podcast API, this operation is `GET /podcast.xml` (base URL `https://feeds.npr.org/510289`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-episodes.md) for the provider-specific parameters and requirements.

