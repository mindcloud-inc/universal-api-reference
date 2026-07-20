# Mercado Pago Universal API Examples

These examples use the MindCloud API key and Mercado Pago connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payment Methods

Retrieves payment methods from Mercado Pago.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "payment_type_id": "string",
      "secure_thumbnail": "string",
      "status": "string",
      "thumbnail": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Payment Methods action reference](actions/list-payment-methods.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mercadoPago/latest/actions/list-payment-methods).

## Create Cancellation

Cancels a payment in Mercado Pago.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-cancellation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payment_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/create-cancellation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payment_id": 1
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Cancellation action reference](actions/create-cancellation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mercadoPago/latest/actions/create-cancellation).
