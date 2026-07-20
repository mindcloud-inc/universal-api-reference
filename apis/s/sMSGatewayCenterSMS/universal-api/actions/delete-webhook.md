# SMSGatewayCenter SMS: Delete Webhook



```
DELETE https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGatewayCenter SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/delete-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/delete-webhook?${params}`, {
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

Through the native SMSGatewayCenter SMS API, this operation is `POST /SMSApi/webhook/delete` (base URL `https://unify.smsgateway.center`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

