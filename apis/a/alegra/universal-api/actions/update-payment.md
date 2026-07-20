# Alegra: Update Payment

Updates an existing payment in Alegra.

```
PUT https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "date": "string",
  "bankAccount.id": 1,
  "paymentMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "date": "string",
    "bankAccount.id": 1,
    "paymentMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `date` | string | yes |  |
| `bankAccount.id` | number | yes |  |
| `paymentMethod` | string | yes |  |
| `observations` | string | no |  |
| `anotation` | string | no |  |
| `type` | string | no |  |
| `client.id` | number | no |  |
| `invoices[].id` | number | no |  |
| `invoices[].amount` | number | no |  |
| `invoices[].retentions[].id` | number | no |  |
| `invoices[].retentions[].name` | string | no |  |
| `invoices[].retentions[].percentage` | number | no |  |
| `invoices[].retentions[].amount` | number | no |  |
| `invoices[].retentions[].currency.code` | string | no |  |
| `invoices[].retentions[].currency.symbol` | string | no |  |
| `invoices[].retentions[].currency.exchangeRate` | number | no |  |
| `bills[].id` | number | no |  |
| `bills[].amount` | number | no |  |
| `bills[].retentions[].id` | number | no |  |
| `bills[].retentions[].name` | string | no |  |
| `bills[].retentions[].percentage` | number | no |  |
| `bills[].retentions[].amount` | number | no |  |
| `bills[].retentions[].currency.code` | string | no |  |
| `bills[].retentions[].currency.symbol` | string | no |  |
| `bills[].retentions[].currency.exchangeRate` | number | no |  |
| `categories[].id` | number | no |  |
| `categories[].tax.id` | number | no |  |
| `categories[].quantity` | number | no |  |
| `categories[].price` | number | no |  |
| `categories[].observations` | string | no |  |
| `retentions[].id` | number | no |  |
| `retentions[].amount` | number | no |  |
| `currency.code` | string | no |  |
| `currency.exchangeRate` | number | no |  |
| `costCenter` | number | no |  |
| `comments[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `PUT /payments/:id` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment.md) for the provider-specific parameters and requirements.

