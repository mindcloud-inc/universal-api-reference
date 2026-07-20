# Ayrshare: Add RSS Feed

Creates a new RSS feed in Ayrshare.

```
POST https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/add-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/add-rss-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "platforms[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/add-rss-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "platforms[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | RSS feed URL to add for automated posting. |
| `platforms[]` | array<string> | yes | Platforms the feed should publish to when new items are found. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "id": "string",
      "message": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `id` | string | Created RSS feed ID. |
| `message` | string | Add feed or error message. |
| `status` | string | Add feed status. |
| `title` | string | Feed title. |
| `url` | string | Feed URL. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /feed` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-rss-feed.md) for the provider-specific parameters and requirements.

