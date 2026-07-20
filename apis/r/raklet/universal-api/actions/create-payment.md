# Raklet: Create Payment



```
POST https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": 1,
  "paymentMethod": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": 1,
    "paymentMethod": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationMembershipId` | string | no |  |
| `amount` | number | yes |  |
| `currency` | number | yes |  |
| `paymentMethod` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": 1,
      "id": "string",
      "isManualPayment": true,
      "isRecurringPayment": true,
      "memberName": "Ava Chen",
      "organisationMembershipId": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": 1,
      "referenceNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdOn` | date |  |
| `currency` | number |  |
| `id` | string |  |
| `isManualPayment` | boolean |  |
| `isRecurringPayment` | boolean |  |
| `memberName` | string |  |
| `organisationMembershipId` | string |  |
| `paymentDate` | date |  |
| `paymentMethod` | number |  |
| `referenceNumber` | string |  |

## Native endpoint

Through the native Raklet API, this operation is `POST /organisations/:organisationId/payments` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

