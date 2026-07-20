# Landbot: Get Customer

Retrieves a customer from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | Customer ID to retrieve. |

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
        "mindcloudVerification": {
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        },
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
      "mindcloudVerification": "string",
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
| `customFields.mindcloudVerification.name` | string |  |
| `customFields.mindcloudVerification.type` | string |  |
| `customFields.mindcloudVerification.value` | string |  |
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
| `mindcloudVerification` | string |  |
| `name` | string |  |
| `optIn` | boolean |  |
| `pausedUntil` | object |  |
| `registerDate` | number |  |
| `ticketId` | object |  |
| `unread` | boolean |  |
| `uuid` | string |  |
| `visitorId` | object |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/customers/:customer_id/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

