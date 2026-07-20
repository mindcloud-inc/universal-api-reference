# CRM Messaging: Send WhatsApp Template

Sends a WhatsApp template from CRM Messaging.

```
POST https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/send-whats-app-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/send-whats-app-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "msg": "string",
  "tempName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/send-whats-app-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "msg": "string",
    "tempName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient phone number with country code. |
| `msg` | string | yes | WhatsApp template body. |
| `tempName` | string | yes |  |
| `mediaUrl` | string | no |  |
| `fromNum` | string | no |  |
| `lang` | string | no |  |
| `dynamicLink` | string | no |  |
| `productId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "msgId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Immediate provider submission result message. |
| `msgId` | string | CRM Messaging outbound message identifier returned on submission. |
| `status` | number | HTTP-style status returned immediately after submission. |

## Native endpoint

Through the native CRM Messaging API, this operation is `POST /index.php/Api/sendMsg` (base URL `https://app.crm-messaging.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-template.md) for the provider-specific parameters and requirements.

