# Discourse: Get Post

Retrieves a single post from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-post?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-post?${params}`, {
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
| `id` | string | yes | Numeric Discourse post ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions_summary": [
        {}
      ],
      "avatar_template": "string",
      "cooked": "string",
      "created_at": "string",
      "id": 1,
      "post_number": 1,
      "post_url": "https://example.com",
      "raw": "string",
      "topic_id": 1,
      "topic_slug": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions_summary` | array<object> |  |
| `avatar_template` | string |  |
| `cooked` | string |  |
| `created_at` | string |  |
| `id` | number |  |
| `post_number` | number |  |
| `post_url` | string |  |
| `raw` | string |  |
| `topic_id` | number |  |
| `topic_slug` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /posts/:id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

