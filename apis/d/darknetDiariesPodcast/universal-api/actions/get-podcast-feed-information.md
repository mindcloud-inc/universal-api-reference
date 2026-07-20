# Darknet Diaries Podcast: Get Podcast Feed Information

Retrieves podcast feed information from Darknet Diaries Podcast.

```
GET https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-feed-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Darknet Diaries Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-feed-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-feed-information?${params}`, {
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
      "atomSelfUrl": "https://example.com",
      "generator": "string",
      "language": "string",
      "lastBuildDate": "2026-05-07T12:00:00.000Z",
      "newFeedUrl": "https://example.com",
      "rssUrl": "https://example.com",
      "title": "string",
      "ttl": 1,
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `atomSelfUrl` | string |  |
| `generator` | string |  |
| `language` | string |  |
| `lastBuildDate` | date |  |
| `newFeedUrl` | string |  |
| `rssUrl` | string |  |
| `title` | string |  |
| `ttl` | number |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Darknet Diaries Podcast API, this operation is `GET /` (base URL `https://podcast.darknetdiaries.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-feed-information.md) for the provider-specific parameters and requirements.

