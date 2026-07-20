# Discourse: Search

Finds Discourse content by search term.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/search?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/search?${params}`, {
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
| `page` | string | no | Search results page number. |
| `q` | string | yes | Search query string using Discourse search syntax. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "grouped_search_result": {},
      "groups": [
        {}
      ],
      "posts": [
        {}
      ],
      "tags": [
        {}
      ],
      "topics": [
        {}
      ],
      "users": [
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
| `categories` | array<object> |  |
| `grouped_search_result` | object |  |
| `groups` | array<object> |  |
| `posts` | array<object> |  |
| `tags` | array<object> |  |
| `topics` | array<object> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /search.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

