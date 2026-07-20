# Xkcd: Get RSS Feed

Retrieves the RSS comic feed from Xkcd.

```
GET https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xkcd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-rss-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-rss-feed?${params}`, {
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
      "item": [
        {}
      ],
      "language": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | RSS channel description or item HTML description. |
| `guid` | string | RSS item stable URL identifier. |
| `item` | array<object> | RSS comic feed entries. |
| `language` | string | RSS feed language. |
| `link` | string | RSS channel or item URL. |
| `pubDate` | string | RSS item publication date. |
| `title` | string | RSS channel or item title. |

## Native endpoint

Through the native Xkcd API, this operation is `GET /rss.xml` (base URL `https://xkcd.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rss-feed.md) for the provider-specific parameters and requirements.

