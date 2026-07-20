# YouTube: List Activities

Retrieves channel activity items from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-activities?${params}`, {
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
| `part` | string | yes | Comma-separated activity resource parts to include. Default: `snippet,contentDetails`. |
| `channelId` | string | no | Return activities for a specific channel. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `home` | boolean | no | Retrieve feed activities from subscriptions. |
| `publishedAfter` | date | no | Return activities published after this timestamp. |
| `publishedBefore` | date | no | Return activities published before this timestamp. |
| `regionCode` | string | no | Region code for regional filtering. |

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

Through the native YouTube API, this operation is `GET /youtube/v3/activities` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

