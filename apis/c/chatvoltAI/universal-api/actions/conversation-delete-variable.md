# Chatvolt AI: Delete Custom Variable

Deletes a custom variable from Chatvolt AI.

```
DELETE https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-delete-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-delete-variable?connectionId=$CONNECTION_ID&conversationId=string&varName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string",
  "varName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-delete-variable?${params}`, {
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
| `varName` | string | yes | Name of the variable to be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | object | Deleted. |
| `message` | string | Message. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `DELETE /variables/{conversationId}/{varName}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-delete-variable.md) for the provider-specific parameters and requirements.

