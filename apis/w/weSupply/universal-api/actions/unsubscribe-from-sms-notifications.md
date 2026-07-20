# WeSupply: Unsubscribe From SMS Notifications

Unsubscribes a customer from WeSupply SMS notifications.

```
DELETE https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/unsubscribe-from-sms-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/unsubscribe-from-sms-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/unsubscribe-from-sms-notifications?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerPhone` | string | no | The customer phone number to unsubscribe. |
| `orderExternalOrderId` | string | no | The external order ID to unsubscribe from SMS updates. |

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
| `message` | string | SMS unsubscription status message returned by WeSupply. |

## Native endpoint

Through the native WeSupply API, this operation is `GET /phone/v2/unsubscribe` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-from-sms-notifications.md) for the provider-specific parameters and requirements.

