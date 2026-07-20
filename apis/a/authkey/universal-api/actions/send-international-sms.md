# Authkey: Send International SMS

Sends an international SMS through Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-international-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-international-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobile": "9999999999",
  "countryCode": "91",
  "sms": "Hello, your OTP is 1234",
  "sender": "SENDERID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-international-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobile": "9999999999",
    "countryCode": "91",
    "sms": "Hello, your OTP is 1234",
    "sender": "SENDERID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mobile` | string | yes | Recipient mobile number. Example: `9999999999`. |
| `countryCode` | string | yes | Recipient country dialing code. Example: `91`. |
| `sms` | string | yes | SMS message content. Example: `Hello, your OTP is 1234`. |
| `sender` | string | yes | Sender ID for the SMS request. Example: `SENDERID`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `GET https://api.authkey.io/request` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-international-sms.md) for the provider-specific parameters and requirements.

