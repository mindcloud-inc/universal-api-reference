# Apple News and Music: List Top Audiobooks (Top 100)

Retrieves the top 100 audiobooks from Apple Books charts.

```
GET https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-audiobooks-top100
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple News and Music `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-audiobooks-top100?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-audiobooks-top100?${params}`, {
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
      "artistName": "Ava Chen",
      "artworkUrl100": "https://example.com",
      "genres": [
        {}
      ],
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artistName` | string | Artist, author, or publisher name. |
| `artworkUrl100` | string | 100x100 artwork image URL. |
| `genres` | array<object> | Apple genre objects for the feed item. |
| `id` | string | Apple feed item identifier. |
| `kind` | string | Apple media kind for the feed item. |
| `name` | string | Apple feed item name or title. |
| `releaseDate` | date | Release or publish date. |
| `url` | string | Apple URL for the item. |

## Native endpoint

Through the native Apple News and Music API, this operation is `GET https://rss.marketingtools.apple.com/api/v2/us/audio-books/top/100/audio-books.json` (base URL `https://itunes.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-audiobooks-top100.md) for the provider-specific parameters and requirements.

