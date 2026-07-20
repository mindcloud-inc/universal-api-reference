# Pop Culture Happy Hour Podcast: List Recent Episodes

Retrieves recent podcast episodes from Pop Culture Happy Hour Podcast.

```
GET https://connect.mindcloud.co/v1/universal/popCultureHappyHourPodcast/latest/actions/list-recent-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pop Culture Happy Hour Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/popCultureHappyHourPodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/popCultureHappyHourPodcast/latest/actions/list-recent-episodes?${params}`, {
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
      "description": "string",
      "duration": 1,
      "enclosure": {},
      "encoded": "string",
      "episodeType": "string",
      "explicit": "string",
      "guid": "string",
      "image": {},
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "thumbnail": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `duration` | number |  |
| `enclosure` | object |  |
| `encoded` | string |  |
| `episodeType` | string |  |
| `explicit` | string |  |
| `guid` | string |  |
| `image` | object |  |
| `link` | string |  |
| `pubDate` | date |  |
| `thumbnail` | object |  |
| `title` | string |  |

## Native endpoint

Through the native Pop Culture Happy Hour Podcast API, this operation is `GET /podcast.xml` (base URL `https://feeds.npr.org/510282/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-episodes.md) for the provider-specific parameters and requirements.

