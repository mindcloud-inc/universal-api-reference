# Oboloo: Create Payment Term

Creates a new payment term in Oboloo.

```
POST https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-payment-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-payment-term" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payment_term_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-payment-term', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payment_term_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payment_term_name` | string | yes | Name of the payment term to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "paymentTerm": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": 1,
        "id": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `paymentTerm.createdAt` | date |  |
| `paymentTerm.createdBy` | number |  |
| `paymentTerm.id` | number |  |
| `paymentTerm.updatedAt` | date |  |
| `paymentTerm.value` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `POST /configuration/addpaymentTerms` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-term.md) for the provider-specific parameters and requirements.

