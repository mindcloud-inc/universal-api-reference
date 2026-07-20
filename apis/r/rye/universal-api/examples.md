# Rye Universal API Examples

These examples use the MindCloud API key and Rye connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Product

Finds a product in Rye by URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "brand": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isPurchasable": true,
      "name": "Ava Chen",
      "price": {},
      "sku": "string",
      "url": "https://example.com",
      "variantDimensions": [
        {}
      ],
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Lookup Product action reference](actions/lookup-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rye/latest/actions/lookup-product).

## Add Payment To Checkout Intent



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rye/latest/actions/add-payment-to-checkout-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "paymentMethod": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/add-payment-to-checkout-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "paymentMethod": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "buyer": {},
      "constraints": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discoverPromoCodes": true,
      "failureReason": {},
      "id": "string",
      "nextAction": {},
      "offer": {},
      "orderId": "string",
      "paymentMethod": {},
      "productUrl": "https://example.com",
      "promoCodes": [
        "string"
      ],
      "quantity": 1,
      "state": "string",
      "variantSelections": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Payment To Checkout Intent action reference](actions/add-payment-to-checkout-intent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rye/latest/actions/add-payment-to-checkout-intent).
