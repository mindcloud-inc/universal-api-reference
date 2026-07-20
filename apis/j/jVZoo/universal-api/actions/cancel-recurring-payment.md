# JVZoo: Cancel Recurring Payment

Cancels a recurring payment in JVZoo.

```
PUT https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/cancel-recurring-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JVZoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/cancel-recurring-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "preKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/cancel-recurring-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "preKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preKey` | string | yes | The key used for the recurring payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canceled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceled` | boolean | Whether the recurring payment was canceled. |

## Native endpoint

Through the native JVZoo API, this operation is `PUT /recurring_payment/:preKey` (base URL `https://api.jvzoo.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-recurring-payment.md) for the provider-specific parameters and requirements.

