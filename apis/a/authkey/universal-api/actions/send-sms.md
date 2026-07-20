# Authkey: Send SMS

Sends an SMS message through Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | no | Recipient country dialing code. |
| `mobile` | string | no | Recipient mobile number. |
| `peId` | string | no | DLT principal entity ID. |
| `sender` | string | no | Sender ID. |
| `sms` | string | no | SMS message content. |
| `templateId` | string | no | DLT template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `GET https://api.authkey.io/request` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

