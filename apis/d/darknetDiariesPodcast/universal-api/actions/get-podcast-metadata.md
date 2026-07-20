# Darknet Diaries Podcast: Get Podcast Metadata

Retrieves podcast metadata from Darknet Diaries Podcast.

```
GET https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Darknet Diaries Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-podcast-metadata?${params}`, {
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
      "author": "string",
      "category": "string",
      "copyright": "string",
      "descriptionHtml": "string",
      "explicit": true,
      "generator": "string",
      "imageUrl": "https://example.com",
      "language": "string",
      "lastBuildDate": "2026-05-07T12:00:00.000Z",
      "newFeedUrl": "https://example.com",
      "ownerEmail": "ava@example.com",
      "ownerName": "Ava Chen",
      "rssUrl": "https://example.com",
      "summary": "string",
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
| `author` | string |  |
| `category` | string |  |
| `copyright` | string |  |
| `descriptionHtml` | string |  |
| `explicit` | boolean |  |
| `generator` | string |  |
| `imageUrl` | string |  |
| `language` | string |  |
| `lastBuildDate` | date |  |
| `newFeedUrl` | string |  |
| `ownerEmail` | string |  |
| `ownerName` | string |  |
| `rssUrl` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `ttl` | number |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Darknet Diaries Podcast API, this operation is `GET /` (base URL `https://podcast.darknetdiaries.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-metadata.md) for the provider-specific parameters and requirements.

