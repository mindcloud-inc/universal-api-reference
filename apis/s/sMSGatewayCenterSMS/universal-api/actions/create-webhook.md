# SMSGatewayCenter SMS: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGatewayCenter SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com",
  "webhookRate": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com",
    "webhookRate": "10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | yes | URL that will receive SMS delivery reports. |
| `webhookRate` | number | yes | DLR TPS rate for forwarding webhook events. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "action": "string",
        "api": "string",
        "code": "string",
        "msg": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.action` | string | Provider action name. |
| `response.api` | string | Provider API family. |
| `response.code` | string | Provider response code. |
| `response.msg` | string | Provider message. |
| `response.status` | string | Provider status label. |

## Native endpoint

Through the native SMSGatewayCenter SMS API, this operation is `POST /SMSApi/webhook/create` (base URL `https://unify.smsgateway.center`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

