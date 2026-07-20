# HelpCrunch: Snooze Chat

Updates a chat's snooze status in HelpCrunch.

```
PUT https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/snooze-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/snooze-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "snoozedUntil": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/snooze-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "snoozedUntil": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `snoozedUntil` | string | yes |  |

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

Through the native HelpCrunch API, this operation is `PUT /chats/snooze` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/snooze-chat.md) for the provider-specific parameters and requirements.

