# Landbot: List Customers

Retrieves customers from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-customers?${params}`, {
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
| `channelId` | number | no | Channel ID of the customers. |
| `agentId` | number | no | Agent ID of the customers. |
| `searchBy` | string | no | Field to search by. |
| `search` | string | no | Value to search; Landbot applies a starts-with match. |
| `archived` | boolean | no | Include archived customers. |
| `optIn` | boolean | no | Filter by WhatsApp opt-in status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": {},
      "archived": true,
      "avatar": "string",
      "blocked": true,
      "brandId": 1,
      "channelId": 1,
      "customFields": {
        "name": {
          "name": "Ava Chen",
          "type": "Ava Chen",
          "value": "Ava Chen"
        }
      },
      "email": {},
      "id": 1,
      "lastMessage": 1,
      "lastMessageContent": "string",
      "lastReceiveDate": 1,
      "lastSendDate": 1,
      "metaData": {
        "apiPayload": "string"
      },
      "name": "Ava Chen",
      "optIn": true,
      "pausedUntil": {},
      "registerDate": 1,
      "ticketId": {},
      "unread": true,
      "uuid": "string",
      "visitorId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | object |  |
| `archived` | boolean |  |
| `avatar` | string |  |
| `blocked` | boolean |  |
| `brandId` | number |  |
| `channelId` | number |  |
| `customFields.name.name` | string |  |
| `customFields.name.type` | string |  |
| `customFields.name.value` | string |  |
| `email` | object |  |
| `id` | number |  |
| `lastMessage` | number |  |
| `lastMessageContent` | string |  |
| `lastReceiveDate` | number |  |
| `lastSendDate` | number |  |
| `metaData.apiPayload` | string |  |
| `name` | string |  |
| `optIn` | boolean |  |
| `pausedUntil` | object |  |
| `registerDate` | number |  |
| `ticketId` | object |  |
| `unread` | boolean |  |
| `uuid` | string |  |
| `visitorId` | object |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/customers/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

