# NewsBlur: Get Original Text

Retrieves a story's original text from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-text?connectionId=$CONNECTION_ID&storyHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-text?${params}`, {
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
| `storyHash` | string | yes | Story hash to fetch extracted full text for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "failed": true,
      "feed_id": 1,
      "original_text": "string",
      "result": "string",
      "story_hash": "string",
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
| `failed` | boolean | Whether extraction failed. |
| `feed_id` | number | Feed ID. |
| `original_text` | string | Extracted original story text or HTML. |
| `result` | string | Result status. |
| `story_hash` | string | Story hash. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /rss_feeds/original_text` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-original-text.md) for the provider-specific parameters and requirements.

