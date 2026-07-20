# Saastic: Create Customer Charge

Creates a customer charge in Saastic.

```
POST https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-customer-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-customer-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-customer-charge', {
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
| `email` | string | no | The customer's email address. Required when phone is not provided. |
| `phone` | string | no | The customer's phone number. Required when email is not provided. |
| `amount` | number | no | Amount of charge in the lowest currency denomination. |
| `currency` | string | no | The 3-letter currency code. |
| `locationSlug` | string | no | The slug of a location. If provided, the default location for the customer will be changed to this one. |
| `chargedAt` | date | no | The date the customer was charged. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "charged_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `charged_at` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `POST /beacon/charges` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-charge.md) for the provider-specific parameters and requirements.

