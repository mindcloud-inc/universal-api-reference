# Rillion Prime Pay: Approve Payments



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-payments" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-payments', {
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
| `processInstantly` | boolean | no | If true, payments will be processed instantly after approval |
| `processAccordingToSchedule` | boolean | no | If true, payments will be processed on the next scheduled date after approval |

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

Through the native Rillion Prime Pay API, this operation is `POST /payment/process/approve` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-payments.md) for the provider-specific parameters and requirements.

