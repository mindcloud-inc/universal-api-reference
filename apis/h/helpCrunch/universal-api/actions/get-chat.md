# HelpCrunch: Get Chat

Retrieves a single chat from HelpCrunch.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-chat?connectionId=$CONNECTION_ID&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-chat?${params}`, {
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
| `chatId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents": [
        {}
      ],
      "applicationId": 1,
      "assignee": {},
      "closedAt": "string",
      "closedBy": "string",
      "createdAt": "string",
      "createdWith": "string",
      "customer": {},
      "department": {},
      "id": 1,
      "lastCommunicatedAgentId": 1,
      "lastCustomerMessageAt": "string",
      "lastMessageAt": "string",
      "lastMessageId": 1,
      "lastMessageText": "string",
      "rating": "string",
      "readByAgent": true,
      "readByCustomer": true,
      "snoozedUntil": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<object> |  |
| `applicationId` | number |  |
| `assignee` | object |  |
| `closedAt` | string |  |
| `closedBy` | string |  |
| `createdAt` | string |  |
| `createdWith` | string |  |
| `customer` | object |  |
| `department` | object |  |
| `id` | number |  |
| `lastCommunicatedAgentId` | number |  |
| `lastCustomerMessageAt` | string |  |
| `lastMessageAt` | string |  |
| `lastMessageId` | number |  |
| `lastMessageText` | string |  |
| `rating` | string |  |
| `readByAgent` | boolean |  |
| `readByCustomer` | boolean |  |
| `snoozedUntil` | string |  |
| `status` | string |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `GET /chats/:chatId` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

