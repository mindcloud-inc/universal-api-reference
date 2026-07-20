# NewsBlur: Mark Feeds As Read

Marks feeds as read in NewsBlur.

```
PUT https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-feeds-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-feeds-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-feeds-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedId` | number | yes | Feed ID to mark as read. NewsBlur supports repeating feed_id for multiple feeds. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cutoffTimestamp` | number | no | Timestamp cutoff for older or newer stories. |
| `direction` | string | no | Whether stories older or newer than the cutoff should be marked as read. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "cutoff_date": "string",
      "direction": "string",
      "errors": [
        "string"
      ],
      "result": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `code` | number | NewsBlur result code. |
| `cutoff_date` | string | Cutoff date used by the update, when provided. |
| `direction` | string | Read direction applied by NewsBlur. |
| `errors` | array<string> | Any errors returned while marking feeds read. |
| `result` | string | Result status. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `POST /reader/mark_feed_as_read` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-feeds-as-read.md) for the provider-specific parameters and requirements.

