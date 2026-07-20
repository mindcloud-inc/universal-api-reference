# Discourse: Get Topic Posts

Retrieves selected posts from a Discourse topic.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-posts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-posts?${params}`, {
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
| `id` | string | yes | Numeric Discourse topic ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "post_stream": {},
      "related_topics": [
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
| `id` | number |  |
| `post_stream` | object |  |
| `related_topics` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /t/:id/posts.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic-posts.md) for the provider-specific parameters and requirements.

