# NewsBlur: List Starred Stories

Retrieves starred stories from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-starred-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-starred-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-starred-stories?${params}`, {
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
| `tag` | string | no | Only load saved stories under a specific tag. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storyHash` | string<string> | no | Story hash to load from saved stories. NewsBlur supports repeating h up to 100 hashes. |
| `highlights` | boolean | no | Only load stories that have highlighting. |
| `query` | string | no | Search keyword or phrase in saved stories. NewsBlur notes feed search is premium-only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "feeds": {},
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
| `feeds` | object | Related feeds keyed by feed ID. |
| `message` | string | Status message. |
| `result` | string | Result status. |
| `stories` | array<object> | Saved stories. |
| `user_id` | number | Authenticated NewsBlur user ID. |
| `user_profiles` | array<object> | Related user profiles. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/starred_stories` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-starred-stories.md) for the provider-specific parameters and requirements.

