# NewsBlur: Get Stories By Hash

Retrieves stories from NewsBlur by story hash.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-stories-by-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-stories-by-hash?connectionId=$CONNECTION_ID&storyHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-stories-by-hash?${params}`, {
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
| `storyHash` | string | yes | Story hash to retrieve. NewsBlur supports repeating h up to 100 hashes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "classifiers": {},
      "code": 1,
      "elapsed_time": 1,
      "hidden_stories_removed": 1,
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
| `classifiers` | object | Feed intelligence classifiers. |
| `code` | number | NewsBlur result code. |
| `elapsed_time` | number | Server processing time. |
| `hidden_stories_removed` | number | Count of hidden stories removed. |
| `message` | string | Status message. |
| `result` | string | Result status. |
| `stories` | array<object> | Stories matching the requested hashes. |
| `user_id` | number | Authenticated NewsBlur user ID. |
| `user_profiles` | array<object> | Related user profiles. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/river_stories` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stories-by-hash.md) for the provider-specific parameters and requirements.

