# Bluesky: Get Feed Generator

Retrieves details for a Bluesky feed generator.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed-generator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed-generator?connectionId=$CONNECTION_ID&feed=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feed": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-feed-generator?${params}`, {
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
| `feed` | string | yes | AT-URI of the feed generator to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isOnline": true,
      "isValid": true,
      "view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isOnline` | boolean |  |
| `isValid` | boolean |  |
| `view` | object |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.feed.getFeedGenerator` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-generator.md) for the provider-specific parameters and requirements.

