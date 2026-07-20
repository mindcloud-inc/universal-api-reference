# Crisp: Remove Conversation

Deletes an existing conversation from Crisp.

```
DELETE https://connect.mindcloud.co/v1/universal/crisp/latest/actions/remove-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/remove-conversation?connectionId=$CONNECTION_ID&websiteId=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/remove-conversation?${params}`, {
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
| `websiteId` | string | yes | The website identifier |
| `sessionId` | string | yes | The conversation session identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crisp API returns.

## Native endpoint

Through the native Crisp API, this operation is `DELETE /website/:website_id/conversation/:session_id` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-conversation.md) for the provider-specific parameters and requirements.

