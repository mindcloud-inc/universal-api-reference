# Alegra: Update Bill

Updates an existing purchase bill in Alegra.

```
PUT https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "date": "string",
  "dueDate": "string",
  "provider": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/update-bill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "date": "string",
    "dueDate": "string",
    "provider": 1
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
| `dueDate` | string | yes |  |
| `observations` | string | no |  |
| `termsConditions` | string | no |  |
| `provider` | number | yes |  |
| `numberTemplate.number` | string | no |  |
| `warehouse` | number | no |  |
| `purchases.items[].id` | number | no |  |
| `purchases.items[].name` | string | no |  |
| `purchases.items[].discount` | number | no |  |
| `purchases.items[].observations` | string | no |  |
| `purchases.items[].tax[].id` | number | no |  |
| `purchases.items[].tax[].name` | string | no |  |
| `purchases.items[].tax[].percentage` | number | no |  |
| `purchases.items[].tax[].description` | string | no |  |
| `purchases.items[].tax[].type` | string | no |  |
| `purchases.items[].tax[].status` | string | no |  |
| `purchases.items[].price` | number | no |  |
| `purchases.items[].quantity` | number | no |  |
| `purchases.items[].total` | number | no |  |
| `purchases.items[].subtotal` | number | no |  |
| `purchases.categories[].id` | number | no |  |
| `purchases.categories[].name` | string | no |  |
| `purchases.categories[].discount` | number | no |  |
| `purchases.categories[].observations` | string | no |  |
| `purchases.categories[].tax[].id` | number | no |  |
| `purchases.categories[].tax[].name` | string | no |  |
| `purchases.categories[].tax[].percentage` | number | no |  |
| `purchases.categories[].tax[].description` | string | no |  |
| `purchases.categories[].tax[].type` | string | no |  |
| `purchases.categories[].tax[].status` | string | no |  |
| `purchases.categories[].price` | number | no |  |
| `purchases.categories[].quantity` | number | no |  |
| `purchases.categories[].total` | number | no |  |
| `purchases.categories[].subtotal` | number | no |  |
| `retentions[].id` | number | no |  |
| `retentions[].amount` | number | no |  |
| `currency.code` | string | no |  |
| `currency.symbol` | string | no |  |
| `currency.exchangeRate` | number | no |  |
| `payments[].date` | string | no |  |
| `payments[].amount` | number | no |  |
| `payments[].account` | string | no |  |
| `payments[].paymentMethod` | string | no |  |
| `payments[].observations` | string | no |  |
| `payments[].anotation` | string | no |  |
| `payments[].retentions[].id` | number | no |  |
| `payments[].retentions[].name` | string | no |  |
| `payments[].retentions[].percentage` | number | no |  |
| `payments[].retentions[].amount` | number | no |  |
| `payments[].currency.code` | string | no |  |
| `payments[].currency.symbol` | string | no |  |
| `payments[].currency.exchangeRate` | number | no |  |
| `costCenter` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `PUT /bills/:id` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bill.md) for the provider-specific parameters and requirements.

