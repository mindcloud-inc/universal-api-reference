# NewsBlur: Save Story

Saves a story in NewsBlur.

```
PUT https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/save-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/save-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/save-story', {
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
| `storyHash` | string | yes | Story hash to save. |
| `userTags[]` | array<string> | no | Tags to apply to the saved story. Accepts multiple values as an array. |
| `highlights[]` | array<string> | no | Strings to highlight on the saved story. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "message": "string",
      "result": "string",
      "starred_count": 1,
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
| `message` | string | Status message. |
| `result` | string | Result status. |
| `starred_count` | number | Total saved story count. |
| `starred_counts` | array<object> | Saved story count details by tag or feed. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `POST /reader/mark_story_hash_as_starred` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-story.md) for the provider-specific parameters and requirements.

