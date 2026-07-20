# Ayrshare: Update RSS Feed

Updates an existing RSS feed in Ayrshare.

```
PUT https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-rss-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-rss-feed', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ayrshare RSS feed ID to update. |
| `url` | string | no | Updated RSS feed URL. |

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
| `id` | string | RSS feed ID. |
| `message` | string | Update feed or error message. |
| `status` | string | Update feed status. |
| `title` | string | Feed title. |
| `url` | string | Feed URL. |

## Native endpoint

Through the native Ayrshare API, this operation is `PUT /feed` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rss-feed.md) for the provider-specific parameters and requirements.

