# Alegra: Create Invoice

Creates a new sales invoice in Alegra.

```
POST https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dueDate": "string",
  "date": "string",
  "client.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dueDate": "string",
    "date": "string",
    "client.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `termsConditions` | string | no |  |
| `numberTemplate.id` | string | no |  |
| `operationType` | string | no | Country-specific invoice versions may require an operation type. Peru accounts commonly use INTERNAL_SALE. Example: `INTERNAL_SALE`. |
| `numberTemplate.prefix` | string | no |  |
| `numberTemplate.number` | string | no |  |
| `items[].id` | string | no |  |
| `items[].name` | string | no |  |
| `items[].discount` | number | no |  |
| `items[].observations` | string | no |  |
| `items[].tax[].id` | string | no |  |
| `items[].price` | number | no |  |
| `items[].quantity` | number | no |  |
| `anotation` | string | no |  |
| `dueDate` | string | yes |  |
| `date` | string | yes |  |
| `observations` | string | no |  |
| `client.id` | string | yes |  |
| `seller` | number | no |  |
| `priceList` | number | no |  |
| `currency` | string | no |  |
| `retentions[].id` | string | no |  |
| `retentions[].amount` | number | no |  |
| `warehouse` | number | no |  |
| `remissions[].id` | string | no |  |
| `remissions[].items[].id` | string | no |  |
| `costCenter` | number | no |  |
| `comments[]` | array<string> | no |  |
| `periodicity` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `POST /invoices` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

