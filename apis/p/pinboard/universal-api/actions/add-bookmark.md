# Pinboard: Add Bookmark



```
POST https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/add-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/add-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/add-bookmark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | Title of the bookmarked page. |
| `dt` | date | no | Bookmark creation time. |
| `extended` | string | no | Longer description for the bookmark. |
| `replace` | boolean | no | Replace an existing bookmark for the same URL. |
| `shared` | boolean | no | Make the bookmark public. |
| `tags` | string | no | Whitespace-separated tags. |
| `toread` | boolean | no | Mark the bookmark as unread. |
| `url` | string | yes | The URL to bookmark. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result_code` | string | Pinboard result code. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/add` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-bookmark.md) for the provider-specific parameters and requirements.

