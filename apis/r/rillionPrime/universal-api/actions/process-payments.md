# Rillion Prime Pay: Process Payments



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/process-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/process-payments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/process-payments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentIds[]": ["string"]
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
| `setScheduledDate` | date | no | Scheduled date to apply to the payment. Only allowed when paymentStatus is PaymentAwaitingApproval or PaymentApproved. Time of day comes from the schedule. |
| `removeScheduledDate` | boolean | no | Set to true to remove the scheduled date and recompute it from the schedule settings. Only allowed when paymentStatus is PaymentCreated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": {
        "duplicateStatus": 1
      },
      "successfull": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed.duplicateStatus` | number |  |
| `successfull` | number |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/process` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-payments.md) for the provider-specific parameters and requirements.

