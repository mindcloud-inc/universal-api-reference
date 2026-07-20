# Apple News and Music: List Apple Newsroom Articles

Retrieves Apple Newsroom articles from the official RSS feed.

```
GET https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-apple-newsroom-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple News and Music `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-apple-newsroom-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/list-apple-newsroom-articles?${params}`, {
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
      "rawXml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawXml` | string | Raw RSS or Atom XML returned by Apple's public feed. |

## Native endpoint

Through the native Apple News and Music API, this operation is `GET https://www.apple.com/newsroom/rss-feed.rss` (base URL `https://itunes.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apple-newsroom-articles.md) for the provider-specific parameters and requirements.

