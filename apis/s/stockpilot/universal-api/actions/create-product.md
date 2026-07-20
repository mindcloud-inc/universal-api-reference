# Stockpilot: Create Product

Creates a new product in Stockpilot.

```
POST https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Codex Product 20260401 1738"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Codex Product 20260401 1738"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Product title Example: `Codex Product 20260401 1738`. |
| `description` | string | no | Product description Example: `Minimal seeded product for Stage 3 testing`. |
| `brand` | number | no | Brand ID Example: `5217`. |
| `category` | number | no | Category ID Example: `8649`. |
| `isActive` | boolean | no | Whether the product is active Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product_id": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product_id` | number | Created Stockpilot product ID |
| `title` | string | Product title |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /products/create` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

