# NewsBlur: List Read Stories

Retrieves read stories from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-read-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-read-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-read-stories?${params}`, {
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
| `order` | string | no | Story order: newest or oldest. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "feeds": [
        {}
      ],
      "message": "string",
      "result": "string",
      "stories": [
        {}
      ],
      "user_id": 1,
      "user_profiles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `feeds` | array<object> | Related feeds. |
| `message` | string | Status message. |
| `result` | string | Result status. |
| `stories` | array<object> | Read stories. |
| `user_id` | number | Authenticated NewsBlur user ID. |
| `user_profiles` | array<object> | Related user profiles. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/read_stories` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-read-stories.md) for the provider-specific parameters and requirements.

