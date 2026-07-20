# SMSGlobal: List Incoming Messages

Retrieves incoming messages from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-incoming-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-incoming-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-incoming-messages?${params}`, {
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
          "campaign": {
            "id": 1
          },
          "dateTime": "2026-05-07T12:00:00.000Z",
          "destination": "string",
          "id": 1,
          "isMultipart": true,
          "isUnicode": true,
          "message": "string",
          "origin": "string",
          "partNumber": 1,
          "totalParts": 1
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
| `limit` | number | Number of incoming message objects returned. |
| `messages[].campaign.id` | number | Associated campaign identifier, when present. |
| `messages[].dateTime` | date | The date and time the message was received. |
| `messages[].destination` | string | The shared pool or dedicated number the SMS was sent to. |
| `messages[].id` | number | Incoming message identifier. |
| `messages[].isMultipart` | boolean | Whether the message spans multiple parts. |
| `messages[].isUnicode` | boolean | Whether the incoming SMS contains Unicode characters. |
| `messages[].message` | string | Incoming SMS content. |
| `messages[].origin` | string | Where the SMS appears to come from. |
| `messages[].partNumber` | number | Part number for multipart messages. |
| `messages[].totalParts` | number | Total number of parts for multipart messages. |
| `offset` | number | Pagination offset. |
| `total` | number | Total number of incoming message objects. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/sms-incoming` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incoming-messages.md) for the provider-specific parameters and requirements.

