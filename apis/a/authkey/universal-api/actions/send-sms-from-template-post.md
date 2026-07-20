# Authkey: Send SMS From Template (POST)

Sends an SMS from a template in Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms-from-template-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms-from-template-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/send-sms-from-template-post', {
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
| `sid` | string | no | SMS template SID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `POST https://console.authkey.io/restapi/requestjson.php` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-from-template-post.md) for the provider-specific parameters and requirements.

