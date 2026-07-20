# Missive: List Conversation Posts

Retrieves posts from a Missive conversation.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-posts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-posts?${params}`, {
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
| `id` | string | yes | Conversation ID. |
| `limit` | number | no | Number of posts returned. Default and max 10. |
| `until` | number | no | Unix timestamp used to paginate with the oldest post created_at value from the previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "conversationIcon": {},
      "createdAt": 1,
      "fromField": {},
      "id": "string",
      "markdown": {},
      "notification": {
        "body": "string",
        "title": "string"
      },
      "references": {},
      "text": "string",
      "username": {},
      "usernameIcon": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `conversationIcon` | object |  |
| `createdAt` | number |  |
| `fromField` | object |  |
| `id` | string |  |
| `markdown` | object |  |
| `notification.body` | string |  |
| `notification.title` | string |  |
| `references` | object |  |
| `text` | string |  |
| `username` | object |  |
| `usernameIcon` | object |  |

## Native endpoint

Through the native Missive API, this operation is `GET /conversations/:id/posts` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-posts.md) for the provider-specific parameters and requirements.

