# ExpertTexting: Send Unicode SMS

Creates a Unicode SMS message in ExpertTexting.

```
POST https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-unicode-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ExpertTexting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-unicode-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "DEFAULT",
  "to": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-unicode-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "DEFAULT",
    "to": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Sender ID or DEFAULT for reliable delivery. Default: `DEFAULT`. |
| `to` | string | yes | Recipient number in international E.164 format without + or 00. |
| `text` | string | yes | Unicode SMS body text, UTF-8 and URL-encoded by the platform. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageCount": 1,
      "messageId": "string",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageCount` | number | Number of SMS message units counted by the provider. |
| `messageId` | string | Provider message ID returned by ExpertTexting. |
| `price` | number | Price returned for the send request. |

## Native endpoint

Through the native ExpertTexting API, this operation is `POST /ExptRestApi/sms/json/Message/Send` (base URL `https://www.experttexting.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-unicode-sms.md) for the provider-specific parameters and requirements.

