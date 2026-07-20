# BBC Sport - Football: List Football Match of the Day Articles



```
GET https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-match-of-the-day-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BBC Sport - Football `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-match-of-the-day-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-match-of-the-day-articles?${params}`, {
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
      "guid": "string",
      "link": "https://example.com",
      "publishedAt": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | RSS item summary or excerpt |
| `guid` | string | RSS item identifier |
| `link` | string | BBC article URL |
| `publishedAt` | string | RSS publication timestamp |
| `thumbnailUrl` | string | RSS thumbnail image URL |
| `title` | string | RSS item title |

## Native endpoint

Through the native BBC Sport - Football API, this operation is `GET /football/match_of_the_day/rss.xml` (base URL `http://newsrss.bbc.co.uk/rss/sportonline_uk_edition`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-football-match-of-the-day-articles.md) for the provider-specific parameters and requirements.

