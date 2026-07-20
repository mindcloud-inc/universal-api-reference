# HelpCrunch: Search Chats

Finds chats in HelpCrunch using search filters.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/search-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/search-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/search-chats?${params}`, {
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

Through the native HelpCrunch API, this operation is `POST /chats/search` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-chats.md) for the provider-specific parameters and requirements.

