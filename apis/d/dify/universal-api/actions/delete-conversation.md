# Dify: Delete Conversation

Deletes an existing conversation from Dify.

```
DELETE https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-conversation?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/delete-conversation?${params}`, {
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
| `conversationId` | string | yes | Conversation ID to delete. |
| `user` | string | no | User identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dify API returns.

## Native endpoint

Through the native Dify API, this operation is `DELETE /conversations/:conversation_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-conversation.md) for the provider-specific parameters and requirements.

