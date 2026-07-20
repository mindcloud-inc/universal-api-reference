# THE HILL: RSS Feed

Retrieves The Hill's news RSS feed.

```
GET https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a THE HILL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/rss-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/rss-feed?${params}`, {
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
| `feed` | string | no | RSS feed name to load. Default: `partnerfeed-news-feed`. |
| `format` | string | no | Feed format to request. Default: `rss`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native THE HILL API returns.

## Native endpoint

Through the native THE HILL API, this operation is `GET /feed/` (base URL `https://thehill.com/wp-json/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rss-feed.md) for the provider-specific parameters and requirements.

