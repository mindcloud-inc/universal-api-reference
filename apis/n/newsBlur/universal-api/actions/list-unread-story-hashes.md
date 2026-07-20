# NewsBlur: List Unread Story Hashes

Retrieves unread story hashes from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-unread-story-hashes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-unread-story-hashes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-unread-story-hashes?${params}`, {
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
| `feedId` | number | no | Feed ID to check. NewsBlur supports repeating feed_id for multiple feeds. |
| `includeTimestamps` | boolean | no | Include timestamps for story dates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "result": "string",
      "unread_feed_story_hashes": {},
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
| `result` | string | Result status. |
| `unread_feed_story_hashes` | object | Unread story hashes keyed by feed ID; values may include timestamps when requested. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/unread_story_hashes` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unread-story-hashes.md) for the provider-specific parameters and requirements.

