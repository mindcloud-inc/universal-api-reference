# Monetizze Universal API Examples

These examples use the MindCloud API key and Monetizze connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Calculate Checkout Installments

Retrieves transparent checkout installment options from Monetizze.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments?connectionId=$CONNECTION_ID&ctk=string&reference=string&value=1&maxInstallments=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ctk": "string",
  "reference": "string",
  "value": "1",
  "maxInstallments": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments?${params}`, {
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
      "msg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Calculate Checkout Installments action reference](actions/calculate-checkout-installments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monetizze/latest/actions/calculate-checkout-installments).

## Process Transparent Checkout Order

Creates a transparent checkout order in Monetizze.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/process-transparent-checkout-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/process-transparent-checkout-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
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
      "msg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Process Transparent Checkout Order action reference](actions/process-transparent-checkout-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/monetizze/latest/actions/process-transparent-checkout-order).
