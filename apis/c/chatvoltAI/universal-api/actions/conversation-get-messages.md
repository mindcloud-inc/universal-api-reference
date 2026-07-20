# Chatvolt AI: Get Messages

Retrieves messages from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-messages?connectionId=$CONNECTION_ID&conversationId=string&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string",
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-messages?${params}`, {
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
| `conversationId` | string | yes | ID of the conversation from which the messages will be retrieved. |
| `count` | number | yes | Number of most recent messages to be retrieved. If not specified, the default is 2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isAiEnabled": true,
      "messages": [
        "string"
      ],
      "organizationId": "string",
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isAiEnabled` | boolean | IsAiEnabled. |
| `messages` | array | Messages. |
| `organizationId` | string | OrganizationId. |
| `status` | string | Status. |
| `userId` | string | UserId. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /conversation/{conversationId}/messages/{count}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-get-messages.md) for the provider-specific parameters and requirements.

