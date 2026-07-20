# SMSGlobal: List Outgoing Messages

Retrieves outgoing messages from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-outgoing-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-outgoing-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-outgoing-messages?${params}`, {
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
      "limit": 1,
      "messages": [
        {
          "dateTime": "2026-05-07T12:00:00.000Z",
          "destination": "string",
          "id": 1,
          "message": "string",
          "origin": "string",
          "outgoing_id": 1,
          "status": "string"
        }
      ],
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of outgoing message objects returned. |
| `messages[].dateTime` | date | The date the message was created in UTC. |
| `messages[].destination` | string | Destination mobile number. |
| `messages[].id` | number | Message part identifier. |
| `messages[].message` | string | Outgoing message content. |
| `messages[].origin` | string | Where the SMS appears to come from. |
| `messages[].outgoing_id` | number | Outgoing message identifier. |
| `messages[].status` | string | Message delivery status. |
| `offset` | number | Pagination offset. |
| `total` | number | Total number of outgoing message objects. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/sms` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-outgoing-messages.md) for the provider-specific parameters and requirements.

