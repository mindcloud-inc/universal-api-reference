# Routee: Send Verification Message

Sends a verification message with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-verification-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-verification-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-verification-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | The phone number in E.164 format (e.g., `+306974444444`). |
| `requestId` | string | no | Unique identifier from the checkSendAbility method |
| `senderUsername` | string | no | Username of the Telegram channel |
| `code` | string | no | Custom verification code (4-8 numeric characters |
| `codeLength` | string | no | Length of the generated verification code (4-8) |
| `callbackUrl` | string | no | HTTPS URL to receive delivery reports |
| `payload` | string | no | Custom payload (0-128 bytes |
| `ttl` | number | no | Time-to-live in seconds (60-86400) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `POST /telegram` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-verification-message.md) for the provider-specific parameters and requirements.

