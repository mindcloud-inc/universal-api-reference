# NewsBlur: Autocomplete Feeds

Finds feeds in NewsBlur by search phrase.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `term` | string | yes | Phrase to search for in feed address, URL, and title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feeds": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feeds` | array<object> | Feed autocomplete suggestions. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /rss_feeds/feed_autocomplete` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-feeds.md) for the provider-specific parameters and requirements.

