# Dwolla: Create Customer Funding Source

Creates a funding source for a Dwolla customer.

```
POST https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-customer-funding-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-customer-funding-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "routingNumber": "string",
  "accountNumber": "string",
  "bankAccountType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-customer-funding-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "routingNumber": "string",
    "accountNumber": "string",
    "bankAccountType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Dwolla customer ID. |
| `name` | string | yes | Funding source display name |
| `routingNumber` | string | yes | Bank routing number |
| `accountNumber` | string | yes | Bank account number |
| `bankAccountType` | string | yes | Bank account type |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dwolla API returns.

## Native endpoint

Through the native Dwolla API, this operation is `POST /customers/[:id]/funding-sources` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-funding-source.md) for the provider-specific parameters and requirements.

