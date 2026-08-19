# Aspire: Create Partial Payment Item



```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-partial-payment-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-partial-payment-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "paymentDate": "string",
  "paymentMethod": "string",
  "paymentReference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-partial-payment-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "paymentDate": "string",
    "paymentMethod": "string",
    "paymentReference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes |  |
| `billingCompany` | string | no | Billing Company and/or Billing Contact are required. |
| `billingContact` | string | no | Billing Company and/or Billing Contact are required. |
| `branchName` | string | no |  |
| `invoiceNumber` | number | no |  |
| `paymentDate` | string | yes |  |
| `paymentMethod` | list<string> | yes |  |
| `paymentNote` | string | no |  |
| `paymentReference` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `POST PartialPayments` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-partial-payment-item.md) for the provider-specific parameters and requirements.

