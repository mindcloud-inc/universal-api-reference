# Authkey: Send Voice Call

Sends a voice call through Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-voice-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-voice-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobile": "9876543210",
  "countryCode": "91",
  "voice": "Hello, your OTP is 1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-voice-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobile": "9876543210",
    "countryCode": "91",
    "voice": "Hello, your OTP is 1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mobile` | string | yes | Recipient mobile number for the voice call. Example: `9876543210`. |
| `countryCode` | string | yes | Recipient country dialing code. Example: `91`. |
| `voice` | string | yes | Voice message text to read during the call. Example: `Hello, your OTP is 1234`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `GET https://api.authkey.io/request` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-voice-call.md) for the provider-specific parameters and requirements.

