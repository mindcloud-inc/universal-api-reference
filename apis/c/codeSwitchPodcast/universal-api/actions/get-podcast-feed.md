# Code Switch Podcast: Get Podcast Feed

Retrieves the Code Switch podcast RSS feed from NPR.

```
GET https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Code Switch Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeSwitchPodcast/latest/actions/get-podcast-feed?${params}`, {
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
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Raw NPR RSS XML payload for the Code Switch podcast feed. |
| `success` | boolean | Whether the feed request succeeded. |

## Native endpoint

Through the native Code Switch Podcast API, this operation is `GET /510312/podcast.xml` (base URL `https://feeds.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-feed.md) for the provider-specific parameters and requirements.

