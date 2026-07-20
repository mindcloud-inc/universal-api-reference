# Cliengo: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-conversations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "channel": "string",
      "clientName": "Ava Chen",
      "companyId": "string",
      "conversationContext": {},
      "creationDate": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "from": "string",
      "id": "string",
      "intercepted": true,
      "isClosed": true,
      "lastMessage": "string",
      "lastMessageDate": "2026-05-07T12:00:00.000Z",
      "lastMessageSender": "string",
      "operatorTags": [
        "string"
      ],
      "participants": [
        {}
      ],
      "persistentLastOperator": "string",
      "phaseHistory": [
        {}
      ],
      "phaseId": "string",
      "status": "string",
      "supportTicket": [
        {}
      ],
      "tags": [
        "string"
      ],
      "type": "string",
      "unreadMessageCount": 1,
      "visitorColor": "string",
      "visitorEmail": "ava@example.com",
      "visitorName": "Ava Chen",
      "visitorPhone": "string",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `channel` | string |  |
| `clientName` | string |  |
| `companyId` | string |  |
| `conversationContext` | object |  |
| `creationDate` | date |  |
| `externalId` | string |  |
| `from` | string |  |
| `id` | string |  |
| `intercepted` | boolean |  |
| `isClosed` | boolean |  |
| `lastMessage` | string |  |
| `lastMessageDate` | date |  |
| `lastMessageSender` | string |  |
| `operatorTags` | array<string> |  |
| `participants` | array<object> |  |
| `persistentLastOperator` | string |  |
| `phaseHistory` | array<object> |  |
| `phaseId` | string |  |
| `status` | string |  |
| `supportTicket` | array<object> |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `unreadMessageCount` | number |  |
| `visitorColor` | string |  |
| `visitorEmail` | string |  |
| `visitorName` | string |  |
| `visitorPhone` | string |  |
| `websiteId` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /conversations` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

