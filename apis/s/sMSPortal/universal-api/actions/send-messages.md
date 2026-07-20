# SMSPortal: Send Messages



```
POST https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/send-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSPortal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/send-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/send-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | One or more SMS messages to send. |
| `sendOptions.testMode` | boolean | no |  |
| `messages[].content` | string | yes | The SMS message text to send. |
| `sendOptions` | object | no |  |
| `messages[].destination` | string | yes | The destination mobile number in international format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sendResponse": {},
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sendResponse` | object | Summary returned by SMSPortal for the send operation, including counts, balance impact, and sample output in test mode. |
| `statusCode` | number | HTTP status code returned by SMSPortal for the send request. |

## Native endpoint

Through the native SMSPortal API, this operation is `POST /BulkMessages` (base URL `https://rest.smsportal.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-messages.md) for the provider-specific parameters and requirements.

