# Chatvolt AI: Create/Update Custom Variable

Creates a custom variable in Chatvolt AI, or updates an existing one.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-upsert-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-upsert-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "varName": "Ava Chen",
  "varValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-upsert-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "varName": "Ava Chen",
    "varValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | ID of the conversation to which the variable belongs. |
| `varName` | string | yes | Variable name (key). |
| `varValue` | string | yes | Variable value. |

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

Through the native Chatvolt AI API, this operation is `POST /variables` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-upsert-variable.md) for the provider-specific parameters and requirements.

