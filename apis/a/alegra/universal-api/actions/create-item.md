# Alegra: Create Item

Creates a new item in Alegra.

```
POST https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | no |  |
| `reference` | string | no |  |
| `price` | number | yes |  |
| `category.id` | string | no |  |
| `inventory.unit` | string | no |  |
| `inventory.unitCost` | number | no |  |
| `inventory.negativeSale` | boolean | no |  |
| `inventory.warehouses[].id` | string | no |  |
| `inventory.warehouses[].initialQuantity` | number | no |  |
| `inventory.warehouses[].minQuantity` | number | no |  |
| `inventory.warehouses[].maxQuantity` | number | no |  |
| `tax` | string | no |  |
| `type` | string | no |  |
| `customFields[].id` | string | no |  |
| `customFields[].value` | string | no |  |
| `subitems[].item.id` | string | no |  |
| `subitems[].quantity` | number | no |  |
| `kitWarehouse.id` | string | no |  |
| `itemCategory.id` | string | no |  |
| `variantAttributes[].id` | string | no |  |
| `variantAttributes[].options[].id` | string | no |  |
| `accounting.inventory` | string | no |  |
| `accounting.inventariablePurchase` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `POST /items` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

