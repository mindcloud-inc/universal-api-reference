# Apple News and Music: List Top Playlists (Top 25)

Retrieves the top 25 playlists from Apple Music charts.

```
GET https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-playlists-top25
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple News and Music `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-playlists-top25?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-top-playlists-top25?${params}`, {
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
| `artistName` | string | Artist, author, publisher, or show name. |
| `artworkUrl100` | string | 100x100 artwork image URL. |
| `genres` | array<object> | Genres attached to the chart result. |
| `id` | string | Apple identifier for the chart result. |
| `kind` | string | Apple chart item type such as songs, albums, playlists, apps, books, podcasts, or audiobooks. |
| `name` | string | Title of the charted item. |
| `releaseDate` | date | Release or publish date when Apple includes one. |
| `url` | string | Apple URL for the chart result. |

## Native endpoint

Through the native Apple News and Music API, this operation is `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/25/playlists.json` (base URL `https://itunes.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-playlists-top25.md) for the provider-specific parameters and requirements.

