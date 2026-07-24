# Rillion Prime Pay: Cancel Payments



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/cancel-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/cancel-payments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentIds[]": [
    "string"
  ],
  "paymentCancellationReason": "HandledExternally"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/cancel-payments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentIds[]": ["string"],
    "paymentCancellationReason": "HandledExternally"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `paymentIds[]` | array<string> | yes |  |
| `paymentCancellationReason` | list<string> | yes | Reason for payment cancellation One of: `HandledExternally`, `SendBack`, `Voided`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "paymentIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `paymentIds[]` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/process/cancel` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-payments.md) for the provider-specific parameters and requirements.

