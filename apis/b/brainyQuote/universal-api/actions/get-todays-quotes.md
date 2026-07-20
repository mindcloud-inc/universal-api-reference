# BrainyQuote: Get Today's Quotes

Retrieves the BrainyQuote quote of the day feed.

```
GET https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-todays-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrainyQuote `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-todays-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brainyQuote/latest/actions/get-todays-quotes?${params}`, {
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
      "guid": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Quote text exactly as provided by the BrainyQuote RSS feed. |
| `guid` | string | Stable BrainyQuote RSS item identifier. |
| `link` | string | BrainyQuote author page URL included with the RSS item. |
| `pubDate` | date | RSS publication date for the quote item. |
| `title` | string | Author name for the quote item. |

## Native endpoint

Through the native BrainyQuote API, this operation is `GET /link/quotebr.rss` (base URL `https://www.brainyquote.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-todays-quotes.md) for the provider-specific parameters and requirements.

