# YouTube: List Subscriptions

Retrieves one or more subscriptions from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-subscriptions?${params}`, {
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
| `part` | string | yes | Comma-separated subscription resource parts to include. Default: `snippet,contentDetails`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | no | Filter subscriptions by channel ID. |
| `id` | string | no | Comma-separated list of subscription IDs. |
| `myRecentSubscribers` | boolean | no | Return recent subscribers for the authenticated channel. |
| `mySubscribers` | boolean | no | Return subscribers for the authenticated channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet` | object |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/subscriptions` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

