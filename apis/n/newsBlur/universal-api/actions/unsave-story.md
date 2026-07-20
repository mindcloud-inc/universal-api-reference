# NewsBlur: Unsave Story

Removes a saved story from NewsBlur.

```
PUT https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/unsave-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/unsave-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/unsave-story', {
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
| `storyHash` | string | yes | Story hash to unsave. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "messages": [
        "string"
      ],
      "result": "string",
      "starred_counts": [
        {}
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
| `messages` | array<string> | Any messages returned by NewsBlur. |
| `result` | string | Result status. |
| `starred_counts` | array<object> | Saved story count details by tag or feed. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `POST /reader/mark_story_hash_as_unstarred` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsave-story.md) for the provider-specific parameters and requirements.

