# Chatvolt AI: Get One Custom Variable

Retrieves a custom variable from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-variable?connectionId=$CONNECTION_ID&conversationId=string&varName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string",
  "varName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-variable?${params}`, {
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
| `conversationId` | string | yes | Conversation ID. |
| `varName` | string | yes | Variable name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "varName": "Ava Chen",
      "varValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string | ConversationId. |
| `varName` | string | VarName. |
| `varValue` | string | VarValue. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /variables/{conversationId}/{varName}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-get-one-variable.md) for the provider-specific parameters and requirements.

