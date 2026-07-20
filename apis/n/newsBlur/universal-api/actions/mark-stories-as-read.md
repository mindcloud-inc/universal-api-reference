# NewsBlur: Mark Stories As Read

Marks stories as read in NewsBlur.

```
PUT https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-stories-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-stories-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/mark-stories-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyHash": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storyHash` | string | yes | Story hash to mark as read. NewsBlur supports repeating story_hash for multiple stories. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "feed_ids": [
        "string"
      ],
      "friend_user_ids": [
        1
      ],
      "result": "string",
      "story_hashes": [
        "string"
      ],
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
| `feed_ids` | array<string> | Feed IDs affected by the update. |
| `friend_user_ids` | array<number> | Friend user IDs affected by the update. |
| `result` | string | Result status. |
| `story_hashes` | array<string> | Story hashes marked as read. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `POST /reader/mark_story_hashes_as_read` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-stories-as-read.md) for the provider-specific parameters and requirements.

