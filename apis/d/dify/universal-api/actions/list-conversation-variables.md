# Dify: List Conversation Variables

Retrieves conversation variables from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-variables?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-variables?${params}`, {
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
| `conversationId` | string | yes | Conversation ID to inspect variables for. |
| `user` | string | no | User identifier. |
| `lastId` | string | no | Cursor for the next page of variables. |
| `variableName` | string | no | Filter variables by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": 1,
      "value": {},
      "valueType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |
| `value` | object |  |
| `valueType` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /conversations/:conversation_id/variables` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-variables.md) for the provider-specific parameters and requirements.

