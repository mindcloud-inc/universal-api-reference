# CRM Messaging: List Messages

Retrieves messages from CRM Messaging.

```
GET https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM Messaging `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages?${params}`, {
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
      "channel": "string",
      "creditsConsumed": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "deliveryStatus": "string",
      "direction": "string",
      "errorCode": "string",
      "from": "string",
      "id": 1,
      "message": "string",
      "msgId": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `creditsConsumed` | number |  |
| `date` | date |  |
| `deliveryStatus` | string |  |
| `direction` | string |  |
| `errorCode` | string |  |
| `from` | string |  |
| `id` | number |  |
| `message` | string |  |
| `msgId` | string |  |
| `to` | string |  |

## Native endpoint

Through the native CRM Messaging API, this operation is `GET /index.php/Api/messageHistory` (base URL `https://app.crm-messaging.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

