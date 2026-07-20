# WeSupply: Subscribe To SMS Notifications

Subscribes a customer to WeSupply SMS notifications.

```
POST https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/subscribe-to-sms-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/subscribe-to-sms-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/subscribe-to-sms-notifications', {
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
| `customerCountryCode` | string | no | The ISO country code for the customer. |
| `customerPhone` | string | no | The customer phone number to subscribe. |
| `customerPhonePrefix` | string | no | The international dialing prefix for the customer phone number. |
| `orderExternalOrderId` | string | no | The external order ID to subscribe for SMS updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | SMS subscription status message returned by WeSupply. |

## Native endpoint

Through the native WeSupply API, this operation is `GET /phone/v2/enrol` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-sms-notifications.md) for the provider-specific parameters and requirements.

