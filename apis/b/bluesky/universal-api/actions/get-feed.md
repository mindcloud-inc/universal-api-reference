# Bluesky: Get Feed

Retrieves posts from a selected Bluesky feed.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed?connectionId=$CONNECTION_ID&feed=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feed": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed?${params}`, {
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
| `feed` | string | yes | AT-URI of the feed generator to read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "feed": [
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
| `cursor` | string |  |
| `feed` | array<object> |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.feed.getFeed` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed.md) for the provider-specific parameters and requirements.

