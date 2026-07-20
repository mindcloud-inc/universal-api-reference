# Workiz: Add Job Payment

Adds a payment to a job in Workiz.

```
PUT https://connect.mindcloud.co/v1/universal/workiz/latest/actions/add-job-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/add-job-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "date": "string",
  "paymentType": "string",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/add-job-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "date": "string",
    "paymentType": "string",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Payment amount. |
| `date` | string | yes | Date and time when payment was made. |
| `paymentType` | string | yes | The type of payment. |
| `reference` | string | no | Optional confirmation number or reference. |
| `uuid` | string | yes | The job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentId` | number |  |

## Native endpoint

Through the native Workiz API, this operation is `POST /job/addPayment/:UUID/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-job-payment.md) for the provider-specific parameters and requirements.

