# Alegra: Update Invoice

Updates an existing sales invoice in Alegra.

```
PUT https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `termsConditions` | string | no |  |
| `numberTemplate.id` | string | no |  |
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
| `dueDate` | string | no |  |
| `date` | string | no |  |
| `observations` | string | no |  |
| `client.id` | string | no |  |
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

Through the native Alegra API, this operation is `PUT /invoices/:id` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

