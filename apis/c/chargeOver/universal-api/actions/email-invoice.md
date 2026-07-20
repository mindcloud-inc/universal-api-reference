# ChargeOver: Email Invoice

Emails an existing invoice from ChargeOver.

```
PUT https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/email-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/email-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/email-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | The ChargeOver invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native ChargeOver API, this operation is `POST /invoice/:invoice_id/_action/email` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-invoice.md) for the provider-specific parameters and requirements.

