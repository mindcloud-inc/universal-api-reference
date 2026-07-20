# Missive: List Conversation Comments

Retrieves comments from a Missive conversation.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-comments?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-comments?${params}`, {
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
| `limit` | number | no | Number of comments returned. Default and max 10. |
| `until` | number | no | Unix timestamp used to paginate with the oldest comment created_at value from the previous page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Missive API returns.

## Native endpoint

Through the native Missive API, this operation is `GET /conversations/:id/comments` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-comments.md) for the provider-specific parameters and requirements.

