# Framework360: List Chat Messages



```
GET https://connect.mindcloud.co/v1/universal/framework360/latest/actions/chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/chat-messages?connectionId=$CONNECTION_ID&conversationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/chat-messages?${params}`, {
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
| `conversationId` | number | yes | Conversation ID to fetch messages for. |
| `page` | number | no | Results page number. |
| `limit` | number | no | Maximum number of messages per page. |
| `query` | string | no | Free-text search term. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `GET chat/messages` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-messages.md) for the provider-specific parameters and requirements.

